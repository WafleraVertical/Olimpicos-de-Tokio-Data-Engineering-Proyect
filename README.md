# Proyecto de Análisis de los Juegos Olímpicos de Tokio 2020

Este repositorio contiene la configuración y los datos utilizados para el análisis de las medallas en los Juegos Olímpicos de Tokio 2020. El proyecto utiliza varios servicios de Azure, incluyendo Data Factory, Databricks, Storage, y Synapse Analytics.

## Contenido del Repositorio

- **Plantillas ARM**: Contienen la configuración de todos los recursos de Azure.
  - `ARMTemplateForFactory.json`: Plantilla de ARM para Data Factory.
  - `ARMTemplateParametersForFactory.json`: Parámetros para la plantilla de ARM.

- **Archivos de Storage**: Datos utilizados en el análisis.
  - `data/`: Directorio que contiene archivos CSV y otros datos relevantes.

- **Cuaderno de Databricks**: Cuaderno utilizado para el análisis de datos.
  - `notebooks/analysis-notebook.ipynb`: Cuaderno Jupyter exportado de Databricks.

- **Archivos de Power BI**: Reportes y análisis visuales.
  - `powerbi/medals-analysis.pbix`: Archivo de Power BI con el análisis de las medallas.

## Configuración de Recursos

### Data Factory

1. **Importar la Plantilla ARM**:
   - Navega a tu instancia de Data Factory en el portal de Azure.
   - Selecciona "Administrar" y luego "Plantillas".
   - Importa `ARMTemplateForFactory.json` y proporciona los parámetros necesarios desde `ARMTemplateParametersForFactory.json`.

### Databricks

1. **Configuración del Cuaderno**:
   - Sube `notebooks/analysis-notebook.ipynb` a tu instancia de Databricks.
   - Configura y usa una máquina virtual `Standard_DS3_v2`.

### Storage

1. **Cargar Datos**:
   - Los datos se encuentran en el directorio `data/`.
   - Puedes usar Azure Storage Explorer o `az storage` para subir estos archivos a tu cuenta de Azure Storage.

### Synapse Analytics

1. **Configurar Synapse**:
   - Asegúrate de que la configuración de Synapse esté incluida en la plantilla ARM.
   - Importa y configura según sea necesario.

## Análisis de Datos

- Los datos de las medallas y otros resultados se almacenan en archivos CSV.
- El cuaderno de Databricks realiza el análisis de los datos, incluyendo operaciones de limpieza, transformación y visualización.
- El archivo de Power BI proporciona visualizaciones interactivas y reportes del análisis de las medallas.


