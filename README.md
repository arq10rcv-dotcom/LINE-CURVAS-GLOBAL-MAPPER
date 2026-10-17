# LINE · Generador de Curvas de Nivel (Global Mapper)

Aplicación web estática y autónoma para generar curvas de nivel a partir de un predio en KML/KMZ y cotas consultadas a Open-Meteo.

## Abrir

- **En línea:** publica el repositorio con **GitHub Pages** desde la rama `main`, carpeta `/ (root)`; el punto de entrada es [`index.html`](index.html).
- **En tu equipo:** abre `index.html` en Chrome o Edge.

## Funciones

- Importar predios `.kml` y `.kmz`.
- Obtener cotas a través de la API de elevación de Open-Meteo; requiere conexión a Internet para consultar datos nuevos.
- Generar curvas de nivel con intervalos de 0.50 m mediante Marching Squares.
- Recortar las curvas al polígono, suavizarlas y exportarlas en DXF, KML, KMZ o GeoJSON, según las opciones disponibles en la interfaz.

## Datos de prueba

La carpeta [`data/`](data/) contiene un polígono de demostración en KML y KMZ. El DXF de curvas de nivel de ejemplo está conservado dentro del archivo `LINE_CURVAS_GLOBAL_MAPPER_LISTO_GITHUB.zip` disponible en la raíz del repositorio. El visor no carga los archivos automáticamente; puedes importarlos en la interfaz.

## Estructura

```
index.html                            Aplicación principal
LINE_Curvas_Nivel_Global_Mapper.html  Copia alternativa de apertura
LEAME.txt                             Instrucciones originales
data/                                 Predio de ejemplo (KML/KMZ)
LINE_CURVAS_GLOBAL_MAPPER_LISTO_GITHUB.zip  Paquete completo con DXF de muestra
```

## Publicación con GitHub Pages

1. Crea un repositorio independiente llamado `LINE-CURVAS-GLOBAL-MAPPER` en GitHub.
2. Sube los archivos **descomprimidos**, con `index.html` en la raíz del repositorio, a la rama `main`.
3. En **Settings → Pages → Build and deployment**, selecciona **Deploy from a branch**, rama **main**, carpeta **/ (root)** y guarda.
4. Cuando GitHub publique el sitio, estará en `https://arq10rcv-dotcom.github.io/LINE-CURVAS-GLOBAL-MAPPER/` (dirección prevista; solo funciona tras activar Pages).

La interfaz se ejecuta en el navegador: no hay servidor propio, cuenta de usuario ni almacenamiento compartido. Las consultas de elevación dependen de disponibilidad de la API de Open-Meteo.

> Mantener este proyecto independiente de otros repositorios de la misma cuenta.