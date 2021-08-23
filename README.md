# Hackathon RIIAA 2021 "JusticIA para los desaparecidos"

# Extracción de caracteristicas de fichas de personas desaparecidas usando OCR y PLN

**Nombre del equipo**  
Equipo FR13NDS

**Integrantes**

- Gudelia Pilar Pérez Conde
- Jesus Toxqui Ortega
- Miguel Angel Mitzin Izelo
- Miguel Angel Gomez Rojas
- Ángela Margarita Corona González

## Descripión

Reto 2: Extracción de texto:
Se tiene por objetivo realizar la extracción de información de fichas de trabajo que corresponden a expedientes de personas desaparecidas y analizar la información para conocer que les paso.
La información contenida en las fichas de trabajo se encuentran de mala calidad, los archivos están escritos a mano, con mala ortografía, formatos para cada archivo que a la fecha no se tiene claro qué significa.
Como propuesta de solución se plantea un proyecto divido en 2 partes:
1.- Corresponde a la limpieza y extracción de datos, en la que a traves de filtros y tecnicas de OCR se almacenan la información en un archivo csv
2.- Se extrae y analizan los datos de un csv con técnicas de PLN para capturar entidades como nombres, organizaciónes y fechas.

## Pipeline

1. Obtener conjunto de fichas
2. Preprocesamiento de fichas
3. Tesseract OCR
4. Exportar CSV
5. Obtener datos con Pandas
6. Uso de Stop Words
7. Análisis con NLP y Spacy
8. Exportar CSV

## Cómo correr el código

Ejecutar el código JusticIA_ExtraccionDatos.py

1.- Instalar librerías con pip

- [opencv-python 4.5.3.56] (https://pypi.org/project/opencv-python/)
- [os-sys 2.1.4] (https://pypi.org/project/os-sys/)
- [pytesseract 0.3.8] (https://pypi.org/project/pytesseract/)
- [python-csv 0.0.13] (https://pypi.org/project/python-csv/)

  2.- Descargar Tesseract

- Descarga de librería [tesseract] (https://github.com/UB-Mannheim/tesseract/wiki)
- Ejecutar el exe y dar clic en Additional language data donde se seleccionará Math y spanish
  e instalamos.

  3.- Agregar ruta del Tesseract localization en el archivo JusticIA_ExtraccionDatos.py

- pytesseract.pytesseract.tesseract_cmd = r'la_ruta_de_instalacion'

  4.- Agregar la ruta del directorio de imagenes a analizar en el archivo JusticIA_ExtraccionDatos.py

- directorioImagenes = "ruta_del_directorio"

Nota: en caso de no reconocer la ruta intercambiar \ por /

5.- Ejecutar JusticIA_ExtraccionDatos.py

Ejecutar el código JusticIA_AccesoDatos.py

1.- Abrir archivo y ejecutar en jupyter notebook

Nota: Cada bloque contiene un título por cada ejecución
