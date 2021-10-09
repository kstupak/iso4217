# [ISO4217](https://en.wikipedia.org/wiki/ISO_4217) Currencies

This library is a very simple enum containing all currencies listed in the ISO4217.
Enum includes methods to get the name of the currency (in en_US), ISO4217 numerical code and a symbol. Please note, that symbols are not regulated by any standard and are taken from [here](https://en.wikipedia.org/wiki/Currency_symbol) 

### Examples
```php
use ISO4127\Currency;

echo Currency::EUR; //output: EUR
echo Currency::EUR->getName(); //output: Euro
echo Currency::EUR->getISO4217Code(); //output: 978
echo Currency::EUR->getSymbol(); //output: €

print_r(Currency::options());
// output:
// [
//  'AED' => 'United Arab Emirates dirham, د.إ',
//  'AFN' => 'Afghan afghani, ؋',
//  'ALL' => 'Albanian lek, L',
//  ...
// ] 

echo Currency::fromISO4127Code(8)->value; // output: ALL
echo Currency::fromISO4127Code(8)->getName(); // output: Albanian Lek
// same as  
echo Currency::fromISO4127Code('008')->value; // output: ALL
echo Currency::fromISO4127Code('008')->getName(); // output: Albanian Lek
```

You should not rely on the provided `format` function, it is there for quick and dirty work.
Use proper formatting techniques that respect your locale settings.
