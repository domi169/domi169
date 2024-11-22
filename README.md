# CERTAMEN 3: Web Scraping con Selenium y Almacenamiento en MySQL 
### Integrantes: Juan Pablo Bravo - Dominique Tengelin


## Objetivo:
Utilizar Selenium para extraer datos históricos de precios de cierre y volumen de varios instrumentos financieros en Yahoo Finance, almacenar esta información en una base de datos MySQL y realizar consultas y operaciones que incluyan JOINs. También generarán un archivo CSV con los datos recopilados.

## Instrucciones:
### 1. Preparación del Entorno:
Configura Selenium en tu entorno.
Instala y configura un servidor de MySQL. Crea una base de datos llamada finance_data para almacenar los datos obtenidos.

### 2. Extracción de Datos con Selenium:
Usando Selenium, extrae los datos de precios de cierre (close price) y volumen (volume) de los siguientes instrumentos financieros en Yahoo Finance:
- Nasdaq: NQ=F
- Disney: DIS
- Tesla: TSLA
- NVIDIA: NVDA
- DOW: DOW
- Limita la extracción de datos a los últimos 180 días.
- Extrae las columnas de Fecha, Precio de Cierre y Volumen.

### 3. Almacenamiento en MySQL:
Diseña una estructura de tabla para cada instrumento en la base de datos finance_data. Cada tabla debe incluir las siguientes columnas:
- date (fecha)
- close_price (precio de cierre)
- volume (volumen de transacciones)
- Almacena los datos obtenidos en MySQL, con una tabla individual para cada instrumento.

### 4. Generación de CSV:
Exporta la información recopilada a un archivo CSV por cada instrumento financiero (uno para Nasdaq, otro para Disney, etc.), con las mismas columnas usadas en la base de datos (date, close_price, volume).
Incluye los archivos CSV en la entrega final.

### 5. Consultas y Operaciones en MySQL (5 consultas)

## Procedimiento: 
Explicación de cómo configuraron Selenium y MySQL.
Descripción de cómo se implementó el web scraping.
Explicación de cómo se almacenaron los datos, ejemplo de cada consulta SQL y justificación de los JOINs usados.
Entrega el código en un archivo Python (.py o Jupyter Notebook), los archivos CSV con los datos recopilados y un reporte con las consultas de MySQL en un archivo word.

## 1. Configuración de Selenium y MySQL

### Selenium
1. **Instalación de Selenium**:
   Ejecuta el siguiente comando para instalar Selenium:
   pip install selenium
   (pantallazo)

- Instalación del driver de Chrome: (pantallazo)

### MySQL
**Instalación de MySQL**:
 Ejecuta el siguiente comando para instalar MySQL:
   (pantallazo)


## 2. Implementación del Web Scraping
Instrumentos Financieros, se extrajeron datos históricos de Yahoo Finance de los siguientes instrumentos:
- Nasdaq (NQ=F)
- Disney (DIS)
- Tesla (TSLA)
- NVIDIA (NVDA)
- DOW (DOW)

Datos Extraídos, para cada instrumento se extrajeron:
- Fecha (date)
- Precio de cierre (close_price)
- Volumen de transacciones (volume)

## 3. Almacenamiento en MySQL
Estructura de la Base de Datos
Para cada instrumento financiero, se creó una tabla con la siguiente estructura:

## 4. Generación de Archivos CSV
Cada instrumento financiero se exportó a un archivo CSV usando Python: 

## 5. Consultas y Operaciones en MySQL
Consultas realizadas:
- Consulta 1: Extrae las fechas y precios de cierre de los días en que el volumen de Tesla fue superior al de Disney.
- Consulta 2: Encuentra los días en que el precio de cierre de NVIDIA fue superior al del Nasdaq.
- Consulta 3: Calcula el promedio del precio de cierre para cada instrumento financiero.
- Consulta 4: Crea una vista que muestre las fechas y el precio de cierre promedio entre todos los instrumentos en días comunes.
- Consulta 5: Usa un JOIN para combinar datos de Tesla y el DOW, mostrando fechas donde ambos tuvieron un volumen mayor a 10 millones de transacciones.
