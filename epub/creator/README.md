# Creator

Creator crea un proyecto para EPUB con distintas opciones.

## Uso:

  ```
  pc-creator
  ```

## Descripción de los parámetros

### Parámetros opcionales:

* `-d` = [directory] Directorio donde se creará el proyecto.
* `-o` = [output] Nombre del proyecto.
* `-s` = [style sheet] Ruta al archivo CSS que se desea incluir.
* `-c` = [cover] Ruta a la imagen de portada que se desea incluir.
* `-i` = [images] Ruta a la carpeta con las imágenes que se desean incluir.
* `-x` = [xhtml] Ruta a la carpeta con los archivos XHTML que se desean incluir.

### Parámetros únicos:

* `-v` = [version] Muestra la versión.
* `-h` = [help] Muestra la ayuda, la cual es este contenido.
* `--no-pre` = [preliminary] Evita la creación de contenidos preliminares (portada, portadilla y legal).

## Ejemplos

### Ejemplo sencillo:

```
  pc-creator
```

Crea un proyecto EPUB en el directorio actual y con el nombre `epub-creator`.

### Ejemplo en un directorio específico:

```
  pc-creator -d directorio/deseado
```

Crea un proyecto EPUB en `directorio/deseado` y con el nombre `epub-creator`.

### Ejemplo en un directorio y nombre específicos:

```
  pc-creator -d directorio/deseado -o proyecto_epub
```

Crea un proyecto EPUB en `directorio/deseado` y con el nombre `proyecto_epub`.

### Ejemplo en un directorio y nombre específicos, e incluyendo una hoja de estilo:

```
  pc-creator -d directorio/deseado -o proyecto_epub -s ruta/al/archivo.css
```

Crea un proyecto EPUB como el ejemplo anterior, incluyendo la hoja de estilo `archivo.css` en lugar del CSS defecto.

### Ejemplo en un directorio y nombre específicos, e incluyendo una hoja de estilo y una portada:

```
  pc-creator -d directorio/deseado -o proyecto_epub -s ruta/al/archivo.css -c ruta/a/la/portada.jpg
```

Crea un proyecto EPUB como el ejemplo anterior, incluyendo un XHTML que muestra la imagen de `portada.jpg`.

### Ejemplo en un directorio y nombre específicos, e incluyendo una hoja de estilo, una portada y varias imágenes:

```
  pc-creator -d directorio/deseado -o proyecto_epub -s ruta/al/archivo.css -c ruta/a/la/portada.jpg -i ruta/al/directorio/con/imagenes
```

Crea un proyecto EPUB como el ejemplo anterior, incluyendo una copia de las imágenes presentes en `ruta/al/directorio/con/imagenes`.

------

# Notas

## YAML

Este *script* genera un archivo con extensión `.yaml` para los metadatos
del libro. [Consúltese aquí](https://github.com/NikaZhenya/pecas/tree/master/epub/others/yaml)
para mayor información.

## CSS

Al usar `pc-creator` se genera una hoja de estilos CSS por defecto si no se
usa la opción `-s`. Esta plantilla incluye varios elementos que mejoran 
el diseño y estructura del EPUB que pueden [consultarse aquí](https://github.com/NikaZhenya/pecas/tree/master/epub/others/css).
