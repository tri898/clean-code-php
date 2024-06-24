**Simple switch case**
Good
```
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
Better
```
<?php

class Str
{
    private static $currency = [
        'ko' => 'KRW',
        'z-hant' => 'CNY',
        'vn' => 'VND',
    ];

    public function getCurrency()
    {
        return self::currency[$currentLanguage] ?? 'USD';
    }
}
```
