Simple switch case
Good
public function getCurrency() {
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
Better

