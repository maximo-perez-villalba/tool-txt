# tool-txt
La clase TXT agrupa herramientas para trabajar sobre texto al estilo navaja suiza.

## Tools:
### startWith
```php
$txt = TXT::create( "Lorem ipsum..." );
$txt->startWith('Lorem '); //TRUE
```    

### endWith
```php
TXT::create( "Lorem ipsum..." )->endWith('...'); //TRUE
```    

### equals
```php
$text = $otherText = 'Lorem ipsum...';
TXT::create($text)->equals($otherText); //TRUE
```    

### compare
Comparación de string segura a nivel binario.
Devuelve < 0 si $ext es menor que $therText; > 0 si $text es mayor que $otherText y 0 si son iguales. 
@see https://www.php.net/manual/es/function.strcmp.php
```php
$text = $otherText = 'Lorem ipsum...';
TXT::create($text)->compare($otherText) === 0; //TRUE
```    

### contains
```php
TXT::create('Lorem ipsum...')->contains('rem ip'); //TRUE
```    

### lastPart
```php
TXT::create('Lorem|ipsum')->lastPart('|'); //ipsum
TXT::create('Lorem|ipsum')->lastPart('|', TRUE); //|ipsum
```    

### firstPart
```php
TXT::create('Lorem|ipsum')->firstPart('|'); //Lorem
TXT::create('Lorem|ipsum')->firstPart('|', TRUE); //Lorem|
```    

### toCamelCaseClass
```php
TXT::create('mAke_mE camel-case pLEase')->toCamelCaseClass() == 'MakeMeCamelCasePlease'; //TRUE
```    

### toCamelCaseVariable
```php
TXT::create('MAke_mE camel-case pLEase')->toCamelCaseVariable() == 'makeMeCamelCasePlease'; //TRUE
```    


