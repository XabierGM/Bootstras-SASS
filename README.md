# Bootstrap/SASS-parcel

Velaquí un traballo feito con bootstrap e SCSS que inclúe un formulario de inicio de sesión que valida as respostas.

## Proceso

Os primeiros pasos se desenvolveron na terminal de Laragon exactamente como se describían no propio exame. Logo, aplicouse bootstrap mediante o método de importalo dende o javascript creei un formulario personalizado ao meu estilo, con moito javascript. Os estilos fixéronse con SCSS, definindo valores para as cores e o tipo de letra por exemplo e chamándoos polo valor designado cando se precisaban. A través de Javascript levouse a cabo tamén a validación, con patterns no correo (que admite texto, unha arroba, e logo máis texto) e nos apelidos que admite dúas palabras separadas por espazo).

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

## Contribucións

Tutorial sobre formularios de php con bootstrap sacado de [getbootstrap.com](getbootstrap.com)

Gran parte dos estilos tamén veñen dados por bootstrap, así que recoñecementos adicionales para eles.

## Resultados

Se ben sinxela, a páxina recoñece os inputs do usuario e responde positiva ou negativamente a elas dependendo se se segue o patrón ou non, e a páxina ten metido e usado o estilo que lle ven de Bootstrap. Como as ferramentas da consola se usaron ao 100% durante a creación da páxina, damos os obxectivos por conseguidos.

![2022-01-20 14_27_43-Window.png](C:\Users\Usuario\Desktop\2022-01-20%2014_27_43-Window.png)
