# Bootstrap/SASS-parcel

Velaquí un traballo feito con bootstrap e SCSS que inclúe un formulario de inicio de sesión que valida as respostas.

## Proceso

Os primeiros pasos se desenvolveron na terminal de Laragon exactamente como se describían no propio exame. Logo, aplicouse bootstrap mediante o método de importalo dende o javascript creei un formulario personalizado ao meu estilo, con moito javascript. Os estilos fixéronse con SCSS, definindo valores para as cores e o tipo de letra por exemplo e chamándoos polo valor designado cando se precisaban.

```
$body-bg: #25A3FF;
$font-general: 'Roboto', sans-serif;


body {
    margin: 0;
    background: $body-bg;
    font-family: $font-general;
}
```

A través de Javascript levouse a cabo tamén a validación, con patterns no correo (que admite texto, unha arroba, e logo máis texto) e nos apelidos que admite dúas palabras separadas por espazo).

```bash
var questions = [
    {question:"Escriba su nombre"},
    {question:"Escriba sus apellidos", pattern: /^\S+\s\S+$/},
    {question:"Escriba su email", pattern: /^[^\s@]+@[^\s@]+\.[^\s@]+$/},
    {question:"Escriba una contraseña", type: "password"}
]
```

Cando remata o proceso, se se introduciron correctamente os datos, amosa unha pantalla que di ""¡Te damos la bienvenida!"" e o nome que introduciches anteriormente, de maneira similar ao exemplo do libro.

```bash
h1.appendChild(document.createTextNode('¡Te damos la bienvenida, ' + questions[0].value + '!')
```

Para devolver os datos, fixen unha páxina de php chamada login-basico que contén un html sinxelo que simplemente imprime texto plano na pantalla a partir dos datos introducidos durante o formulario. Atópase en dist e en build xa que cada vez que se volvía a construir a páxina a carpeta build borraba o arquivo e debía copialo ahí de novo.

```
<?php
echo "Usuario introducido: ". $_POST['usuario']. "<br>";
echo "Clave introducida: ". $_POST['clave']. "<br>";
echo "Direccción parte 1: ". $_POST['direccion']. "<br>";
echo "Dirección parte 2: ". $_POST['direccion2']. "<br>";
echo "Ciudad: ". $_POST['ciudad']. "<br>";
echo "Código postal: ". $_POST['zip']. "<br>";
```

A ese efecto o formulario volveuse algo máis complexo, con máis campos que se piden.

O proceso de build fíxose, de novo, totalmente coa consola de laragon.

## Contribucións

Tutorial sobre formularios de php con bootstrap sacado de [getbootstrap.com](getbootstrap.com)

Gran parte dos estilos tamén veñen dados por bootstrap, así que recoñecementos adicionales para eles.

## Resultados

Se ben sinxela, a páxina recoñece os inputs do usuario e responde positiva ou negativamente a elas dependendo se se segue o patrón ou non, e a páxina ten metido e usado o estilo que lle ven de Bootstrap. Como as ferramentas da consola se usaron ao 100% durante a creación da páxina, damos os obxectivos por conseguidos.



![2022-01-24 10_37_58-Window.png](C:\Users\Usuario\Desktop\2022-01-24%2010_37_58-Window.png)

![2022-01-24 10_38_14-Window.png](C:\Users\Usuario\Desktop\2022-01-24%2010_38_14-Window.png)
