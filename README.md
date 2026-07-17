# 📍 Local Supplier Data Collector (Maps to CSV)

Una herramienta ligera de recolección de datos diseñada para extraer información de comercios y proveedores locales desde el explorador o Google Maps (a partir de búsquedas específicas como *"proveedores de arcilla cerca de mí"*) y convertirla automáticamente en un archivo **CSV** estructurado.

El objetivo exclusivo de este repositorio es servir como una **herramienta de prueba e ingesta de datos (scraping/recolección)**. La información recolectada y exportada se utiliza para alimentar, probar y validar una aplicación principal externa (por ejemplo, una plataforma con mapa interactivo que conecta creadores y compradores con proveedores locales).

---

## 💡 Propósito y Flujo de Trabajo

Para desarrollar una plataforma que conecte a creadores (ej. un escultor que busca arcilla o pintura especializada) con distribuidores cercanos, primero se necesitan datos reales para hacer pruebas. Esta herramienta resuelve ese primer paso:

1. **Recolección de Datos:** Realiza búsquedas de suministros y materiales específicos directamente en el navegador o Google Maps en una zona determinada.
2. **Transformación:** Extrae los datos clave de los comercios encontrados (nombre del proveedor, dirección, coordenadas GPS y notas de oferta o catálogo) y limpia la información.
3. **Exportación para Pruebas:** Genera un archivo `.csv` estandarizado que se puede importar de inmediato en el proyecto principal para probar el renderizado de mapas, filtros de distancia y comparativas de precios u ofertas.

---

## 📦 Estructura del CSV de Salida

El archivo generado devolverá los datos con las columnas necesarias para que una aplicación externa pueda leer las coordenadas y mostrar las opciones sin necesidad de pre-procesamiento adicional:

```csv
Proveedor,Material_Buscado,Direccion,Latitud,Longitud,Detalle_Oferta
"Suministros Arte & Arcilla","Clay / Arcilla para modelar","101 Creative Way, Ciudad",26.5628,-81.9495,"$15.00 / kg - En stock"
"Pinturas y Pigmentos Sur","Pintura acrílica y óleos","204 Maker Blvd, Ciudad",26.5640,-81.9510,"Descuento mayorista disponible"
