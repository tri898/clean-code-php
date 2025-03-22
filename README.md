# Simple switch case or if else condition

Good
```
<?php

class Ulities
{
  public function getCurrency(string $language)
  {
        switch ($language) {
          case 'ko':
            $currency = 'KRW';
            break;
            
          case 'z-hant':
            $currency = 'CNY';
            break;
    
          case 'vn':
            $currency = 'VND';
            break;

          default:
            $currency = 'USD';
        }
    return $currency;
  }
```
Better
```
<?php

class Ulities
{
    private static $currency = [
        'ko' => 'KRW',
        'z-hant' => 'CNY',
        'vn' => 'VND',
    ];

    public function getCurrency($language)
    {
        return self::currency[$language] ?? 'USD';
    }
}
```
# Avoid If else condition nested
Not Good
```
<?php

class Ulities
{
  public function getCurrency()
  {
    $currency = 'USD';
        switch ($currentLanguage) {
          case 'ko':
            $currency = 'KRW';
            break;
            
          case 'z-hant':
            $currency = 'CNY';
            break;
    
          case 'vn':
            $currency = 'VND';
            break;
        }
    return $currency;
  }
```
# Medthod name, variable có ý nghĩa

# Dùng trait hợp lý


# Áp dụng single responsibility
