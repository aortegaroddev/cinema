# Cinema

Aplicacion Android para explorar series de television mediante la API publica de [TVMaze](https://www.tvmaze.com/api). La pantalla principal presenta el catalogo; cada serie tiene una ficha con informacion, puntuacion, generos, reparto, sitio oficial y un video de muestra. La app tambien ofrece temas claro, oscuro y del sistema.

## Requisitos

- Android Studio con soporte para Android Gradle Plugin 9.3.3
- JDK 17 y Android SDK Platform 37
- Dispositivo o emulador con Android 8.0 (API 26) o posterior
- Conexion a Internet para compilar y cargar datos e imagenes

El proyecto incluye Gradle Wrapper, por lo que no hace falta instalar Gradle por separado. No requiere clave de TVMaze.

## Compilar y probar

Desde la raiz del proyecto:

```bash
./gradlew test
./gradlew assembleDevDebug
```

El APK de desarrollo se genera en `app/build/outputs/apk/dev/debug/`. Para compilar otras variantes:

```bash
./gradlew assembleProdDebug
./gradlew assembleProdRelease
```

La variante `dev` habilita logging y usa `com.hellby.cinema.dev`; `prod` usa `com.hellby.cinema` y deshabilita logging.

## Ejecutar

Con un emulador iniciado o un dispositivo conectado:

```bash
./gradlew installDevDebug
```

Tambien se puede abrir el proyecto en Android Studio y ejecutar la configuracion `app`.

## Tecnologia

Kotlin, Jetpack Compose, Material 3, Hilt, Retrofit, Kotlin Serialization, OkHttp, Coil, Navigation Compose, DataStore y AndroidX Media3.

Los datos se obtienen de [TVMaze](https://www.tvmaze.com/); consulta sus [terminos de uso](https://www.tvmaze.com/api#terms) antes de redistribuir la aplicacion. El video es un recurso remoto de demostracion.
