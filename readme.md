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
**Przypisanie wartości do zmiennej**
```js
let zmienna = 5;
//lub
let zmienna;
zmienna = 5;
//lub
var zmienna = 5;
//lub
var zmienna;
zmienna = 5;
```
> [!WARNING] 
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
> [!NOTE]
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
> [!NOTE]
>**Postać else-if działa tak jak postać ogólna ale daje nam możliwość dodania większej ilości warunków za pomocą ``else if``**
# Pętle

W js mamy trzy rodzaje pętli

**Pętla ``while``**
```js
while (warunek) {
    //kod
}
```
*Przykład użycia:*
```js
let i = 0;

while (i < 10) {
    console.log("i=" + i);
    i++;
}
//program wypisze liczby nastepujaca
/*
i=0
i=1
i=2
i=3
i=4
...
i=9
*/
```
> [!IMPORTANT] 
>**Znaki ``--`` i ``++`` to ``--`` - dekrementacja i ``++`` inkrementacja. Dekrementacja zmniejsza o 1 a inkrementacja zwieksza o 1**

**Pętla ``for``**
```js
for (zmienna; warunek petli; dzialanie na zmiennej) {
    //kod
}
```
*Przykład użycia:*
```js
for (let i = 10; i > 0; i--) {
    console.log("i=" + i);
}

//program wypisze liczby nastepujaca
/*
i=10
i=9
i=8
i=7
i=6
...
i=1
*/
```
**``do .. while``**
```js
do {
    //kod
} while (warunek)
```
*Przykład użycia:*
```js
let i = 0;
do {
    console.log("i=" + i);
    i++;
} while (i < 10)

//program wypisze liczby nastepujaca
/*
i=0
i=1
i=2
i=3
i=4
...
i=9
*/
```

# Tablice (Array)
> [!NOTE]
>**Tablica to zbiór wartości, które można przechowywać w jednej zmiennej. Możemy dostosować rozmiar tablicy używając operatora []**.
```js
let tablica = [];
tablica[0] = 1;
tablica[1] = 2;
tablica[2] = 3;
console.log(tablica); // Wyświetli: [1, 2, 3]
```

# Funkcje
> [!NOTE]
>**Funkcje to bloki kodu, które można powtarzać bezpośrednio w programie. Definiujemy je za pomocą słowo kluczowego function.**

```js
function nazwaFunkcji(parametry) {
    // Kod funkcji
}

function suma(a, b) {
    return a + b;
}

console.log(suma(5, 3)); // Wyświetli: 8
```

# Funkcje matematyczne
> [!NOTE]
>**Funkcja ``Math.pow()`` oblicza potęgę dwóch argumentów.**

```js
console.log(Math.pow(2, 3)); // Wyświetli: 8
```

> [!NOTE]  
>**Funkcja ``Math.random()`` generuje losowe liczby z zakresu [0, 1).**
```js
console.log(Math.random()); // Generuje liczbę losową
```
>[!TIP]
>**Możesz pomnożyć lub dodać liczbę do Math.random() aby wylosować liczbe o innym przedziale**
```js
Math.floor(Math.random() * 100) //liczba całkowita (int) z zakresu [0, 100)

(Math.random() * 100) + 1 //liczba z zakresu [1, 100)
```
> [!NOTE]  
>**Funkcja ``Math.floor()`` zaokrągluje liczbę do całkowitej w dół.**

```js
console.log(Math.floor(3.7)); // Wyświetli: 3
```

# Dom (Document Object Model)

**Główne metody do użycia HTML w js**
> [!NOTE]  
>**Metoda ``getElementById()`` zwraca element DOM o określonym identyfikatorze.**

```js
let element = document.getElementById('id');
element.innerHTML = 'Gówno xd';
```

> [!NOTE]  
>**``innerHTML`` umożliwia manipulowanie zawartością HTML, podczas gdy ``innerText`` działa tylko z tekstem.**

```js
document.getElementById('container').innerHTML = '<h1>Pedał</h1>';
document.getElementById('text').innerText = 'chuj';
```

> [!NOTE]  
>**Atrybut ``style`` pozwala na modyfikację właściwości CSS elementu.**

```js
let div = document.getElementById("div");
div.style.backgroundColor = "blue";
div.style.color = "white";
div.style.width = "200px";
```

# EventListener i podpięcia funkcji w JS w HTML

> [!NOTE]  
>**Metoda ``addEventListener()`` umożliwia podpięcie event listenera do elementu.**

```js
function kliknij () {
    alert("chuj");
}

button.addEventListener("click", kliknij);
```

## Podpięcia funkcji JS w HTML

Możemy również podpiąć event listenera bezpośrednio w HTML.

```js
<button onclick="alert('Kliknięto przycisk!')">Kliknij mnie</button>
```
> [!NOTE]  
>**Event click jest emitowany, gdy użytkownik kliknie element.**
```js
document.getElementById('myButton').addEventListener('click', function() {
    console.log('Przycisk został kliknięty');
});
```

## Podstawowe efektu myszy

> [!CAUTION]
>**``function() {}`` to jest po prostu funkcja ale bez nazwy uzywasz jej tylko w ``addEventListener`` *przykłady poniżej***

> [!NOTE]  
>**mouseover: Emitowany, gdy kursor znajduje się nad elementem.**
```js
element.addEventListener('mouseover', function() {
    this.style.backgroundColor = 'yellow';
});
```
> [!NOTE]  
>**mouseout: Emitowany, gdy kursor opuszcza element.**
```js
element.addEventListener('mouseout', function() {
    this.style.backgroundColor = '';
});
```
> [!NOTE]  
>**mousedown: Emitowany, gdy użytkownik naciśnie klawisz myszy nad elementem.**

```js
element.addEventListener('mousedown', function() {
    console.log('Naciśnięto klawisz myszy');
});
```
> [!NOTE]  
>**mouseup: Emitowany, gdy użytkownik puszczę klawisz myszy nad elementem.**

```js
element.addEventListener('mouseup', function() {
    console.log('Uwolniono klawisz myszy');
});
```

>[!IMPORTANT]
>**Wszystkich efektów myszy podanych powyżej możesz użyć równiesz w elemencie html dodajesz tylko ``on`` *na przykład* ``onmouseup``**
