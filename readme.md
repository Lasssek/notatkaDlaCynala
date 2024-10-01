# Zmienne
Mamy trzy rodzaje zmiennych:
```js
//globalna
var zmienna;
//lokalna zmienna
let zmienna;
//lokalna stała - czyli się nie zmienia
const zmienna;
```
>**Ze zmienna const nie możesz zrobić tak bo bedzię bład!**
```js
const zmienna = 5;
zmienna = 2; //nie przejdzie
```
# Instrukcje warunkowe
### Inaczej if if-else

Mamy trzy sposoby na zapisanie instrukcji if

**Postać ogólna**
```js
if (warunek) {
    //pewien kod
} else {
    //Blok jesli warunek nie zostanie spelniony
}
```
**Postać niepełna**
```js
if (warunek) {
    //pewnie blok kodu
}

//dalsza czesc kodu
```
>**Postać niepełna instrukcji warunkowej *if* wykonuje pewny blok kodu jesli jej warunek sie spelni, jesli nie to wykonuje sie dalsza czesc programu.**

**Postać else-if**
```js
if (warunek) {
    //kod
} else if (warunek) {
    //kod
} else {
    //kod jesli zaden warunek nie zostal spelniony 
}
```
>**Postać else-if działa tak jak postać ogólna ale daje nam możliwość dodania większej ilości warunków za pomocą ``else if``**

# Pętle

