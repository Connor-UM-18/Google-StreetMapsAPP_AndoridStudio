# Tarea 4: Geolocalización y Mapas en Android
#Autor: Connor Urbano Mendoza
Este proyecto de Android implementa la visualización de mapas y la geolocalización del usuario utilizando dos proveedores de mapas diferentes: OpenStreetMap y Google Maps. La aplicación permite al usuario cambiar entre ambas implementaciones a través de una interfaz de pestañas (tabs).

## Descripción

La aplicación cumple con los siguientes requisitos:

* **OpenStreetMap Implementation:**
    * Muestra la ubicación actual del usuario en un mapa de OpenStreetMap.
    * Utiliza la biblioteca Leaflet.js para la interacción con el mapa dentro de un `WebView`.
    * Obtiene las coordenadas del usuario mediante `FusedLocationProviderClient`.
    * Coloca un marcador en la ubicación actual con la etiqueta "Mi ubicación".
    * Maneja los permisos de ubicación en tiempo de ejecución.
* **Google Maps Implementation:**
    * Muestra la ubicación actual del usuario utilizando la versión web de Google Maps cargada en un `WebView`.
    * También utiliza `FusedLocationProviderClient` para obtener la ubicación.
* **Navegación:**
    * Permite al usuario cambiar entre las implementaciones de OpenStreetMap y Google Maps mediante una interfaz de pestañas (tabs).

## Cómo Descargar y Ejecutar

1.  **Requisitos Previos:**
    * Android Studio instalado
    * Dispositivo Android físico o emulador
    * **JDK 17** (Este proyecto ha sido desarrollado y probado con JDK 17. Asegúrese de tener JDK 17 configurado en su Android Studio.)
2.  **Descargar el Repositorio:**
    * Clone este repositorio en su máquina local usando Git:
        ```bash
        git clone <URL_DEL_REPOSITORIO>
        ```
3.  **Abrir el Proyecto en Android Studio:**
    * Abra Android Studio y seleccione "Open an Existing Project".
    * Navegue hasta la carpeta donde clonó el repositorio y seleccione el directorio del proyecto.
4.  **Configurar el SDK de Android:**
    * Asegúrese de tener instalado el SDK de Android necesario para compilar el proyecto. Android Studio debería sugerirle si falta alguno.
5.  **Ejecutar la Aplicación:**
    * Conecte su dispositivo Android o inicie un emulador.
    * En Android Studio, haga clic en el botón "Run" (o presione Shift + F10) para compilar y ejecutar la aplicación en su dispositivo/emulador.
6.  **Permisos de Ubicación:**
    * La aplicación solicitará permisos de ubicación. Asegúrese de otorgar los permisos para que la aplicación pueda mostrar la ubicación del usuario.

## Estructura del Proyecto

El proyecto se estructura de la siguiente manera:

* `MainActivity.kt`:   Maneja la interfaz de pestañas y la navegación entre las actividades de OpenStreetMap y Google Maps.
* `OpenStreetMapActivity.kt`:  Implementa la funcionalidad de OpenStreetMap utilizando Leaflet.js y un `WebView`.
* `GoogleMapsActivity.kt`:   Implementa la funcionalidad de Google Maps utilizando un `WebView`.
* `map.html` (en la carpeta `assets`): Contiene el código HTML y JavaScript (Leaflet.js) para mostrar el mapa de OpenStreetMap.
* `activity_main.xml`, `activity_openstreetmap.xml`, `activity_google_maps.xml`:  Archivos de diseño para las actividades.

## Notas Adicionales

* Este proyecto utiliza `FusedLocationProviderClient` para obtener la ubicación del usuario.
* El rendimiento y la apariencia de la aplicación pueden variar según el dispositivo y la versión de Android.
* Asegúrese de tener una conexión a Internet para que los mapas se carguen correctamente.
* Recuerde que este proyecto **requiere JDK 17** para su correcta compilación y ejecución.
