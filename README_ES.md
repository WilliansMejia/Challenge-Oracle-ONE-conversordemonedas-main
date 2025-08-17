
<img align=left src="https://i.imgur.com/P9fjzh4.png" height=150 alt="badge-challenge">

<h2 align=center>Challenge ONE Back End - Java</h2>

<div align=center>

<img height="80" margin="10" src="https://i.imgur.com/9Gq6RS0.png">
</div>

### Sprint 01: Crea tu propio conversor de moneda

<br> 

## Historia

En esta oportunidad se nos solicitó a nosotros, los Devs, la creación de un conversor de moneda utilizando el lenguaje Java. 
Las características solicitadas por nuestro cliente son las siguientes:

El conversor de moneda deberá:

- Convertir de Reales a Dólar
- Convertir de Reales a Euro
- Convertir de Reales a Libras Esterlinas
- Convertir de Reales a Peso Argentino
- Convertir de Reales a Peso Chileno

Recordando que también debe ser posible convertir en forma inversa.

Como desafío extra, se incentiva a dejar fluir la creatividad. 
Si es posible convertir monedas, ¿será que también puedo agregar a mi programa otro tipo de conversiones, como temperatura, por ejemplo?

<br>



### Conversión

- Las unidades de conversión están divididas en **Clases**. 
  Cada clase posee sus unidades en forma de atributo estático (que sería una instancia de la Clase). 
  Cada unidad tiene un **símbolo**, un **factor multiplicador** (que es usado en el método para realizar la conversión entre unidades) y su **nombre**.
- Una unidad puede ser **convertida a otra** llamando a su propio método convert, de la siguiente forma:

```java
BigDecimal result = REAL.convert(new BigDecimal("1"), DOLAR);
```

⚠️ El factor multiplicador de las monedas es el valor equivalente de 1 en relación al Dólar, para facilitar la conversión entre ellas.

### Interfaz Gráfica (GUI)

- [x] Conforme a lo sugerido para este Challenge, se utilizó el kit de componentes GUI propio de Java, llamado **Swing**, 
  donde podemos crear componentes e interfaces gráficas con el paradigma orientado a objetos.

- [x] Fácil expansión y adición de nuevas unidades de conversión
- Para agregar nuevas unidades, basta crear una subclase
  de <a href="https://github.com/HugoJhonathan/Challenge-Oracle-ONE-conversordemoedas/blob/main/src/main/java/units/Unit.java">
  Unit</a>.
- Para añadir la pantalla referente a esa nueva unidad de conversión basta con:

  1- Crear una clase que extienda la clase abstracta 
  <a href="https://github.com/HugoJhonathan/Challenge-Oracle-ONE-conversordemoedas/blob/main/src/main/java/GUI/screens/Screen.java">
  Screen</a>.

  2- Implementar y concretar los métodos abstractos.

  3- Agregar esa nueva pantalla al objeto en la NavBar, 
  conforme a <a href="https://github.com/HugoJhonathan/Challenge-Oracle-ONE-conversordemoedas/blob/main/src/main/java/GUI/Window.java#L27">
  estos</a>.
- Para crear cualquier otra pantalla, basta con crear una clase que extienda de JPanel e implemente la 
  interfaz <a href="https://github.com/HugoJhonathan/Challenge-Oracle-ONE-conversordemoedas/blob/main/src/main/java/GUI/ScreenProperties.java">
  Screen_Properties</a> y añadirla a la NavBar.

<br>

## Tecnologías utilizadas

- Lenguaje: Java 8
- IDE: <a href="https://www.jetbrains.com/idea/">IntelliJ IDEA</a>
- Interfaz (GUI): Swing con <a href="https://www.formdev.com/flatlaf/">FlatLaf</a>
- Pruebas: <a href="https://junit.org/junit5/">JUnit</a>
- Currency API: <a href="https://docs.awesomeapi.com.br/api-de-moedas">AwesomeAPI-api-de-moedas</a>

<br><br>
[<img align="left" height="50" margin="10" src="https://i.imgur.com/RYYUpCK.png">](https://www.oracle.com/br/education/oracle-next-education/)
Aplicación de Escritorio de **Conversor de Unidades** desarrollada como Challenge, durante la formación Backend Java, del
programa <a href="https://www.oracle.com/br/education/oracle-next-education/">ONE (Oracle Next Education)</a> a través de la
plataforma de enseñanza <a href="https://www.alura.com.br/">Alura</a>.
