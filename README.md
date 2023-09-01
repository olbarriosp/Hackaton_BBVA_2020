# Hackaton_BBVA_2020
NOMBRE DEL RETO: RETO INTERPRETADOR INTELIGENTE
NOMBRE DEL PROYECTO: Aleph Interpreter
GRUPO: TIBURON


El objetivo de nuestra solución, Aleph Interpreter, es garantizar -al funcionario del Banco BBVA-, accesibilidad, óptimo procesamiento, y calidad en la extracción de datos valiosos de los documentos de los estados financieros de PYMES, con el fin de facilitar el proceso de análisis crediticio del banco. Para esto se puso a disposición una página web con la cual aseguramos el uso de nuestra solución desde cualquier dispositivo. En esta página el colaborador del banco podrá cargar documentos en formato pdf asociados a sus posibles clientes. El proceso de análisis se apoya mediante el servicio de Textract AWS y librerías de software libre. Se usarán estrategias de expresiones regulares y diccionarios para extraer las variables solicitadas por el reto Interpretador Inteligente. El colaborador podrá ver reflejado en la página web una visualización previa de la extracción. Una vez validada la información, el usuario podrá descargar en diferentes formatos para su fácil integración. Debido a los controles de  seguridad que ofrece AWS (https://aws.amazon.com/es/textract/) y nuestra página web, no se almacenará ningún documento.

**Extracción y análisis del texto:**
* Configuramos las credenciales de AWS para tener acceso a la API.
* Utilizamos la librería re para extraer la información de cada una de las variables pedidas en el reto con respecto a las expresiones regulares realizadas por el equipo.
* utilizamos la librería pandas para cargar con total libertad nuestros documentos y expresarlos como dataframes y adicionalmente moldear sus filas y columnas de manera que el procesamiento de los datos se haga de manera más ordenada.
* Utilizamos la librería Json para manejar los datos que nos retorna la API de Textract.
* Utilizamos la API de Textract haciendo uso de Boto3 para obtener tablas y texto que se extrae de las páginas
* Utilizamos la librería Pickle para serializar objetos obtenidos a partir de solicitudes a textract.
* La librería de Spacy juega un papel fundamental en nuestro análisis de la información pues su módulo de NLP (procesamiento de lenguaje natural) nos permite, entre otras cosas, analizar el contexto de las palabras o las frases contenidas en los documentos.

