🛍️ My Retail

Aplicación móvil Android desarrollada en Kotlin para gestionar y visualizar información de vendedores de una empresa del rubro retail.

El proyecto fue desarrollado como parte de la asignatura Herramientas de Programación Móvil, integrando recursos multimedia, cámara, almacenamiento de imágenes, audio, video, animaciones y gráficos personalizados.

📱 Descripción

My Retail es una aplicación orientada a reconocer y destacar el desempeño de los vendedores.

La aplicación permite:

👥 Visualizar un listado de cinco vendedores.

🖼️ Mostrar información e imágenes representativas de cada vendedor.

🔊 Reproducir un audio asociado al vendedor destacado.

📷 Capturar fotografías utilizando la cámara del dispositivo.

💾 Gestionar el almacenamiento de fotografías mediante MediaStore.

📊 Visualizar un gráfico de barras con las ventas realizadas.

🎬 Reproducir un video promocional.

✨ Incorporar recursos visuales y animaciones para mejorar la experiencia de usuario.

🚀 Funcionalidades principales

👥 Listado de vendedores

La aplicación muestra cinco vendedores con su información comercial:

Vendedor

Área

Ventas

Roberto

Horeca

150

Augusto

Retail

130

Monica

Mayorista

180

Gabriela

Horeca

145

Raul

Retail

160

Cada vendedor se presenta mediante una tarjeta que incluye:

Imagen representativa.

Nombre.

Área de trabajo.

Cantidad de ventas realizadas.

El vendedor con mayor cantidad de ventas es:

🏆 Monica – 180 ventas

🔊 Reproducción de audio

La aplicación incorpora contenido de audio asociado a la interacción con el listado de vendedores.

El recurso de audio se encuentra integrado dentro de los recursos multimedia del proyecto y permite demostrar la utilización de reproducción de sonido en Android.

Archivo utilizado:

app/src/main/res/raw/vendedor_destacado.wav

📷 Cámara y captura de fotografías

My Retail permite capturar una fotografía utilizando la cámara del dispositivo Android.

La funcionalidad permite:

Acceder a la cámara.

Capturar una fotografía.

Obtener la imagen generada.

Mostrar la fotografía dentro de la aplicación.

Gestionar su almacenamiento como contenido multimedia.

Permiso utilizado:

<uses-permission android:name="android.permission.CAMERA" />

💾 Almacenamiento con MediaStore

Las fotografías capturadas pueden ser gestionadas utilizando las herramientas de almacenamiento multimedia proporcionadas por Android.

Se utiliza:

MediaStore

ContentResolver

Uri

Esta implementación permite trabajar con imágenes generadas durante la ejecución de la aplicación y almacenarlas como contenido multimedia del dispositivo.

📊 Gráfico de ventas

La aplicación incorpora una pantalla destinada a comparar visualmente las ventas realizadas por los vendedores.

Resultados

Total de ventas: 765

Promedio por vendedor: 153,0

Mejor vendedor: Monica

Ventas del mejor vendedor: 180

El gráfico se implementa mediante una vista personalizada.

Entre los componentes utilizados se encuentran:

View

Canvas

Paint

onDraw()

drawRect()

drawText()

invalidate()

Archivo principal del gráfico:

grafico/GraficoBarrasView.kt

🎬 Video promocional

La aplicación incorpora un video promocional relacionado con la identidad de My Retail.

El usuario puede acceder a una pantalla específica para:

▶️ Reproducir el video.

⏸️ Pausar la reproducción.

⏪ Retroceder.

⏩ Avanzar dentro del contenido.

Archivo multimedia:

app/src/main/res/raw/retail_video.mp4

✨ Animaciones

El proyecto incorpora recursos de animación para mejorar la presentación de los elementos visuales.

Recursos incluidos:

app/src/main/res/anim/animacion_contenido.xml
app/src/main/res/anim/animacion_logo.xml

🧰 Tecnologías utilizadas

Tecnología

Uso

Kotlin

Lenguaje principal de desarrollo

Android Studio

Entorno de desarrollo

Android SDK

Plataforma de desarrollo móvil

XML

Diseño de interfaces

RecyclerView

Visualización del listado de vendedores

MediaStore

Gestión de contenido multimedia

MediaPlayer / APIs multimedia

Reproducción de audio

Componentes de video Android

Reproducción de video

Canvas

Dibujo del gráfico

Paint

Configuración visual del gráfico

Camera

Captura de fotografías

📂 Estructura principal del proyecto

Carlos_DiPiazza_HERPM1305_15/
│
├── app/
│   ├── src/main/
│   │   ├── java/com/example/carlos_dipiazza_herpm1305_15/
│   │   │   ├── MainActivity.kt
│   │   │   │
│   │   │   ├── camara/
│   │   │   │   └── CamaraActivity.kt
│   │   │   │
│   │   │   ├── grafico/
│   │   │   │   ├── DatosVentas.kt
│   │   │   │   ├── GraficoBarrasView.kt
│   │   │   │   └── GraficoVentasActivity.kt
│   │   │   │
│   │   │   ├── vendedores/
│   │   │   │   ├── Vendedor.kt
│   │   │   │   ├── VendedorAdapter.kt
│   │   │   │   └── VendedoresActivity.kt
│   │   │   │
│   │   │   └── video/
│   │   │       └── VideoActivity.kt
│   │   │
│   │   ├── res/
│   │   │   ├── anim/
│   │   │   ├── drawable/
│   │   │   ├── layout/
│   │   │   ├── raw/
│   │   │   └── values/
│   │   │
│   │   └── AndroidManifest.xml
│   │
│   └── build.gradle.kts
│
├── gradle/
├── build.gradle.kts
├── gradle.properties
├── settings.gradle.kts
├── gradlew
└── gradlew.bat

🖥️ Pantallas de la aplicación

🏠 Pantalla principal

Presenta:

Logotipo de My Retail.

Nombre de la aplicación.

Mensaje institucional.

Acceso al listado de vendedores.

Acceso a la cámara.

Acceso al gráfico.

Acceso al video promocional.

👥 Vendedores

Permite visualizar:

Roberto.

Augusto.

Monica.

Gabriela.

Raul.

Cada vendedor presenta información relacionada con su área y ventas realizadas.

📷 Fotografía del vendedor destacado

Permite:

Capturar una fotografía.

Utilizar la cámara del dispositivo.

Mostrar la imagen obtenida.

Gestionar el almacenamiento multimedia.

📊 Gráfico de ventas

Permite comparar las ventas de los cinco vendedores mediante barras.

Los datos utilizados son:

Roberto  → 150
Augusto  → 130
Monica   → 180
Gabriela → 145
Raul     → 160

🎬 Video promocional

Permite reproducir un recurso audiovisual relacionado con My Retail.

⚙️ Requisitos para ejecutar el proyecto

Para ejecutar el proyecto se recomienda contar con:

Android Studio.

Android SDK configurado.

JDK compatible con la configuración del proyecto.

Un emulador Android o dispositivo físico.

Permisos de cámara habilitados en caso de utilizar la función de captura.

▶️ Instalación y ejecución

1. Clonar el repositorio

git clone <URL-DEL-REPOSITORIO>

2. Abrir el proyecto

Abrir la carpeta del proyecto desde Android Studio.

3. Esperar la sincronización

Android Studio descargará y sincronizará las dependencias configuradas mediante Gradle.

4. Seleccionar un dispositivo

Puedes utilizar:

Un emulador Android.

Un teléfono Android conectado mediante USB.

5. Ejecutar

Presiona:

Run ▶

o utiliza el comando:

./gradlew assembleDebug

En Windows:

gradlew.bat assembleDebug

📸 Evidencias

El proyecto fue probado en un dispositivo Android, verificando el funcionamiento de:

Instalación de la aplicación.

Pantalla principal.

Listado de vendedores.

Captura de fotografías.

Visualización de imágenes.

Gráfico de ventas.

Reproducción de video.

Para mejorar la presentación del repositorio se recomienda agregar las capturas dentro de una carpeta:

docs/images/

Por ejemplo:

docs/images/inicio.jpg
docs/images/vendedores.jpg
docs/images/camara.jpg
docs/images/grafico.jpg
docs/images/video.jpg

Luego pueden mostrarse en este README utilizando:

![Pantalla principal](docs/images/inicio.jpg)

🎯 Objetivo académico

Este proyecto tiene como objetivo aplicar conocimientos relacionados con el desarrollo de aplicaciones móviles Android, especialmente en las áreas de:

Desarrollo de interfaces móviles.

Kotlin.

Integración multimedia.

Reproducción de audio.

Reproducción de video.

Captura de fotografías.

Uso de la cámara.

Almacenamiento de contenido multimedia.

Uso de MediaStore.

Animaciones.

Construcción de gráficos personalizados.

👨‍💻 Autor

Carlos Di Piazza

Proyecto desarrollado para la asignatura:

Herramientas de Programación Móvil

📄 Licencia

Este proyecto fue desarrollado con fines académicos y educativos.
