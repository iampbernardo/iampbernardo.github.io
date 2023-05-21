+++
title = "Macbook: Dos gestores de paquetes para una instalación más automatizada"
date = "2023-05-21T:07:30+02:00"
author = "Pablo Bernardo"
authorTwitter = "" #do not include @
cover = ""
tags = ["macOS", "Terminal"]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = true
hideComments = false
color = "" #color from the theme settings
draft = false
+++

El fin de semana pasado me puse a hacer limpieza de primavera en el portátil; la primera limpieza de software a fondo desde 2023.

Unido a la idea de eliminar programas inncesarios, porquería acumulada con las actualizaciones y malas configuraciones, me propuse experimentar algo a nivel técnico. Quería ver cuanto de la preparación del portátil desde cero sería capaz de hacer de manera rápida a traves de scripts, sin utilizar ninguna solución comercial para __enrollment__ de dispositivos y en cuanto tiempo. Aunque no ha sido sorpresa, se me ha hecho patente que necesito  mejorar mis habilidades en ``bash scripting``. Hablaremos de ello más adelante.

Para una instalación lo más automatizada, personalizada y desatendida posible, hacen falta varias herramientas. Principalmente una terminal, conexión a internet y un par de métodos para poder cubrir la gestión de aplicaciones desde línea de comandos.

Como parte de mi proyecto de tener un entorno de **Tecnología Resiliente**, te dejo la recomendación de las dos herramientas que yo he incorporado a mi flujo de trabajo: Homebrew y mas-cli. Este post no es un tutorial, sólo una pista para tirar del hilo de posibilidades.

## Homebrew
``url:`` [https://brew.sh/](https://brew.sh/)

Homebrew (o Brew) es un gestor de paquetes para Mac, o Linux, por línea de comandos.

Quizá ya lo conoces. O es posible que, como yo, lo hayas utilizado alguna vez pero de manera desordenada cuando aparecía en algún tutorial online. Yo esta vez me propuse entender un poco mejor sus flujos de trabajo e incorporarlo como parte de los míos.

En el caso de que estés preparando una instalación de Mac más automatizada o quieras gestionar el software y actualizaciones de una manera más personalizada, tienes que conocer Homebrew.

- Brew está basado en Git
- permite la instalación y actualización de paquetes
- Puedes crear tus propias fórmulas

Además, a través de **Hombre Cask** también es posible instalar aplicaciones de interfaz gráfica sin necesidad de ir a una web, descargar imagen, arrastar icono...

## mas-cli
``url:`` [https://github.com/mas-cli/mas](https://github.com/mas-cli/mas)

Hay aplicaciones que no están disponibles a través de Hombrew o que sólo se pueden instalar pasando por el App store. Pero esto corta el rollo y rompería el flujo de trabajo automatizado que intentamos conseguir. Ahí es donde **mas-cli** nos salva la papeleta. Por cierto que mas-cli se instala desde Homebrew 😉.

mas-cli es una herramienta de terminal, con la que puedes gestionar también la instalación, actualizaciones, ports y demás para aplicaciones que se distribuyen a través del App store.

Eso sí, para trabajar con mas-cli, conviene tener presentes un par de cosas.

La primera es que puedes hacer búsquedas por nombre de aplicación desde la consola, pero de cara a la gestión posterior de lo paquestes, esto es instalación, actualizaciones, desinstalaciones y demás, mas hace uso del id de la aplicación en el App Store. Te recomiendo que eches un ojo a la documentación para que no tene pase como a mi con el primer par de instalaciones. Puedes sacar la ``id`` con un ``mas search [nombre de la app]`` y no hace falta ir a buscarlo a la url de la applicación en el navegador; sí, lo sé, a la segunda me di cuenta de que no tenía sentido.

La segunda, debido a algunos cambios en el sistema de macOS, a día de hoy hace flata loguearse en tu cuenta de icloud a través de interfaz gráfica para la gestión de las aplicaciones de App Store. Es un mal menor pero estaría muy bien si consiguieran hacerlo funcionar de nuevo en las versiones más recientes del sistema.




