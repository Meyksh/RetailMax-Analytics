# Document Heading Datos: Entidad + atributos

**Clasificación:**|**Almacenamiento de datos:**||**Procesamiento de datos transaccionales**|**Procesamiento de datos analíticos**|**Arquitecturas de almacenamiento y gestión de datos.**|
|1.Datos estructurados|*1. Almacenes de archivos*|*2. Bases de datos*|El trabajo que realizan los sistemas transaccionales a menudo se conoce como procesamiento de transacciones en línea (OLTP).Base de datos está diseñada para atender muchas operaciones pequeñas y frecuentes con rapidez (lectura y escritura)|Modelo de procesamiento analítico en línea (OLAP)suele utilizar sistemas de solo lectura.|Lago de datos (Data Lake): Es un espacio donde se almacena una gran cantidad de datos en diferentes formatos, incluso sin organizarlos previamente en tablas.
|2.Datos semiestructurados (JSON)|1.1 Archivos de texto delimitado|2.1 Bases de datos relacionales|Aplican transacciones que admiten la denominada semántica ACID.||Almacén de datos (Data Warehouse): Es un sistema que organiza los datos en estructuras preparadas para realizar consultas, elaborar informes y analizar resultados.
|3.Datos no estructurados|1.2 Notación de objetos JavaScript (JSON).|2.2 Bases de datos no relacionales|*Registrar operaciones diarias.*|*Analizar datos y apoyar decisiones.*|Lago de datos híbrido (Data Lakehouse): Es una arquitectura que combina el almacenamiento flexible de un Data Lake con capacidades de gestión y consulta analítica propias de un Data Warehouse.|
|4.Datos vectoriales|1.3 Lenguaje de marcado extensible (XML)|2.2.1 Bases de datos de clave-valor|*Crear, consultar, actualizar y eliminar registros (CRUD)*|*Consultar, comparar y resumir grandes volúmenes de datos.*||
||1.4 Objeto binario grande (BLOB)|2.2.2 Bases de datos de documentos|*Datos actuales y detallados.*|Datos *Históricos, acumulados y agregados.*||
||1.5 Formatos de archivo optimizados|2.2.3 Bases de datos de familia de columnas|Consultas *Cortas y específicas.*|Consultas *Complejas y sobre muchos registros.*||
||1.5.1 Parquet (Guarda por columnas)|2.2.4 Bases de datos de grafos|*Sistemas Típicos Bases de datos operativas.*|Sistemas típicos *Data Warehouse, Data Lakehouse y modelos OLAP.*||
||1.5.2 Avro (Guarda por filas)|||||
||1.5.3 Delta Lake|||||

**DATOS:**

Número y/o descripciones que se usan para registrar información.

&#x20;

Los datos se componen de:

1.Entidad

Estructura del dato (nombre que le dan al dato y los agrupa como conjunto, ej: cliente, producto, pedido de venta.

2.Atributos

Característica de la entidad, eventos específicos u otra información en documentos, videos, audios  ej: nombre, dirección, contacto.

**Clasificación de los datos:**

**1.Datos estructurados:**

Son aquellos que se ajustan a un esquema fijo, por lo que todos los datos tienen los mismos campos o propiedades. Normalmente, el esquema de las entidades de datos estructurados es tabular; es decir, los datos se representan en una o varias tablas que constan de filas para representar cada instancia (presentación) de una entidad de datos y columnas para representar los atributos de la entidad.

**2.Datos semiestructurados:**

Son información que tiene cierta estructura, pero que permite alguna variación entre las instancias (presentación) de entidad. Por ejemplo, aunque la mayoría de los clientes pueden tener una dirección de correo electrónico, algunos podrían tener varias y otros, ninguna.

**3.Datos no estructurados:**

Por ejemplo, los documentos, imágenes, datos de audio y de vídeo y archivos binarios podrían no tener una estructura específica.

**4.Datos vectoriales:**

(también llamados embeddings), que es una representación numérica del contenido, como texto o imágenes. Las aplicaciones de inteligencia artificial usan datos vectoriales para buscar contenido que sea semánticamente similar.

**Almacenamiento de datos:**

*1.Almacenes de archivos*
**1.1 Archivos de texto delimitado**

Los datos se almacenan como texto sin formato con delimitadores de campo y terminadores de fila específicos

El formato más común para los datos delimitados son los valores separados por comas (CSV) Opcionalmente, la primera línea puede incluir los nombres de campo.

Ej: FirstName,LastName,Email

Joe,Jones,<joe@litware.com>

Samir,Nadoy,<samir@northwind.com>

también existe los valores separados por tabulaciones (TSV) y delimitados por espacios (en los que se usan tabulaciones o espacios para separar los campos), así como datos de ancho fijo en los que a cada campo se le asigna un número fijo de caracteres.

**1.2 Notación de objetos JavaScript (JSON).**

JSON es un formato ampliamente usado en el que se usa un esquema de documento jerárquico para definir entidades de datos (objetos) que tienen varios atributos. Cada atributo puede ser un objeto (o una colección de objetos ), lo que hace de JSON un formato flexible adecuado tanto para datos estructurados como semiestructurados.

Ej: Cada cliente tiene tres atributos (firstName, lastName y contact) y el atributo contact contiene una colección de objetos que representan uno o varios métodos de contacto (correo electrónico o teléfono).

Un JSON es un formato para organizar y transmitir datos entre sistemas, aplicaciones y páginas web.

¿Cómo se ve un JSON?

Imagina que tienes una tienda online y alguien compra un par de zapatos. La información de esa venta podría organizarse así:

EJEMPLO DE JSON

{

&#x20; "pedido": 1052,

&#x20; "cliente": "María",

&#x20; "producto": "Zapatos",

&#x20; "cantidad": 2,

&#x20; "total": 40.00,

&#x20; "pagado": true

}

***Cada elemento tiene dos partes:***

***- Clave: el nombre del dato. Por ejemplo, "cliente".***

***- Valor: la información asociada. Por ejemplo, "María".***

¿*Qué debes reconocer en un JSON?*

Elemento/ Ejemplo / Significado

Texto / "cliente": "María" / Se escribe entre comillas dobles.

Número / "cantidad": 2 / No necesita comillas.

Booleano / "pagado": true / Indica verdadero o falso.

Lista / "tallas": \[20, 21, 22] / Agrupa varios valores.

Objeto / "dirección": {"ciudad": "Panamá"} / Agrupa datos relacionados.

*En resumen: JSON es una manera estandarizada de empaquetar información para que una aplicación pueda enviársela a otra y esta pueda interpretarla.*

**1.3 Lenguaje de marcado extensible (XML)**
En gran medida lo ha reemplazado el formato JSON, menos detallado, pero todavía hay algunos sistemas que usan XML para representar datos. XML usa etiquetas entre corchetes angulares (<.. />) para definir elementos y atributos

**1.4 Objeto binario grande (BLOB)**
Es un tipo de dato que permite almacenar grandes cantidades de información binaria, como imágenes, archivos PDF, videos o documentos, dentro de una base de datos.

**1.5 Formatos de archivo optimizados**
Aunque los formatos legibles para datos estructurados y semiestructurados pueden ser útiles, normalmente no están optimizados para el procesamiento o el espacio de almacenamiento. Con el paso del tiempo, se han desarrollado algunos formatos de archivo especializados que permiten la compresión, la indexación y un almacenamiento y procesamiento eficientes.

***1.5.1 Parquet:***
Es un formato para guardar datos de manera organizada, de modo que sea más rápido consultarlos y ocupen menos espacio.

Organiza los datos por columnas.

Producto Ciudad Unidades  Venta

Zapatos         Panamá 3   60

Camisas         Colón 5   75

Bolsos         Panamá 2   40

Zapatos         David 4   80

Es especialmente útil cuando necesitas analizar solo algunas columnas, por ejemplo, las ventas.

Parquet incluye metadatos que describen el conjunto de filas que hay en cada fragmento.

***1.5.2 Avro***
Organiza los datos por filas

Guarda toda la información de cada venta junta.

Venta 1 → Zapatos, Panamá, 3, 60

Venta 2 → Camisas, Colón, 5, 75

Venta 3 → Bolsos, Panamá, 2, 40

Es útil cuando necesitas leer los datos completos de cada venta.

Cada archivo contiene un encabezado que describe la estructura de los datos del archivo. Este encabezado se almacena como JSON

***Característica           Avro                                              Parquet***

Organización           Por filas                                      Por columnas

Cómo describe los datos   Utiliza un esquema almacenado en el encabezado     Utiliza metadatos que describen la estructura y organización del archivo

Almacenamiento           Datos binarios                              Datos organizados por columnas en formato binario

Uso destacado           Intercambio y procesamiento de registros      Análisis de grandes volúmenes de datos

Compresión           Sí                                              Sí

Ejemplo                   Transmitir una venta completa                      Analizar solo la columna de ventas

***1.5.3 Delta Lake***
Utiliza archivos Parquet y un registro de transacciones para controlar cómo cambian los datos.

Ese registro ayuda a evitar que una operación incompleta deje los datos en un estado inconsistente (transacciones ACID, control de versiones de datos y actualizaciones confiables sobre los archivos almacenados en un lago de datos).
 *2. Bases de datos*
**2.1 Bases de datos relacionales**

Las bases de datos relacionales suelen usarse para almacenar y consultar datos estructurados. Las tablas se administran y consultan mediante el Lenguaje de consulta estructurado (SQL)

SQL, Structured Query Language (lenguaje de consulta estructurada) , es un lenguaje que se utiliza para consultar, registrar, modificar y eliminar información almacenada en una base de datos. SQL te permite darle instrucciones a una base de datos para trabajar con sus datos.

¿SQL es lo mismo que MySQL?

No. Esta diferencia es importante:

\- SQL: el lenguaje utilizado para dar instrucciones.

\- MySQL: un sistema gestor de bases de datos que utiliza SQL.

\- PostgreSQL: otro sistema gestor que utiliza SQL.

\- SQLite: un sistema de base de datos ligero que también utiliza SQL.

Una analogía sencilla: SQL es el idioma y MySQL es uno de los sistemas que entiende ese idioma.

**2.2 Bases de datos no relacionales**
Las bases de datos no relacionales son sistemas de administración de datos que no aplican un esquema relacional a los datos. A menudo, las bases de datos no relacionadas se conocen como NoSQL base de datos, aunque algunas admiten una variante del lenguaje SQL.

Bases de datos no relacionales de uso común

2.2.1 Bases de datos de clave-valor

En las que cada registro consta de una clave única y un valor asociado, que puede estar en cualquier formato.

2.2.2 Bases de datos de documentos

Que son una forma específica de base de datos de clave-valor, en la que el valor es un documento JSON (que el sistema está optimizado para analizar y consultar).

2.2.3 Bases de datos de familia de columnas

Que almacenan datos tabulares con filas y columnas, pero con la posibilidad de dividir esas columnas en grupos, conocidos como familias de columnas. Cada familia de columnas contiene un conjunto de columnas que tienen una relación lógica entre sí.

2.2.4 Bases de datos de grafos

Que almacenan entidades como nodos con vínculos para definir relaciones entre ellas.

**Procesamiento de datos transaccionales**
Un sistema transaccional registra las transacciones que encapsulan eventos específicos que la organización desea realizar un seguimiento.

¿Qué significa que las operaciones se aplican transaccionalmente?

Significa que una operación puede incluir varios pasos que deben completarse correctamente como una unidad.

Ej: una venta de un producto que cuesta $20:

1\. Registrar la venta.

2\. Descontar una unidad del inventario.

3\. Registrar el pago.

Si el sistema registra la venta, pero falla al descontar el inventario, podría quedar información contradictoria.

Una base de datos transaccional permite establecer que los pasos relacionados se confirmen juntos o que se reviertan si la operación falla, según cómo esté diseñada la transacción.

El trabajo que realizan los sistemas transaccionales a menudo se conoce como **procesamiento de transacciones en línea (OLTP).**

**Las soluciones OLTP** se basan en un sistema de base de datos en el que el almacenamiento de datos está optimizado para operaciones de lectura y escritura (Significa que la base de datos está diseñada para atender muchas operaciones pequeñas y frecuentes con rapidez ej: una farmacia con 61 sucursales:

\- Un cajero registra una venta.

\- Otro empleado consulta el inventario.

\- Un supervisor actualiza el precio de un medicamento.

\- Un administrador registra el pago de un proveedor.

El sistema debe poder atender estas operaciones sin tener que analizar toda la información de la empresa cada vez.

Por eso, OLTP está pensado para el funcionamiento diario del negocio, no principalmente para elaborar grandes informes históricos.) para admitir cargas de trabajo transaccionales en las que se crean, recuperan, actualizan y eliminan los registros de datos (a menudo denominados operaciones CRUD). Estas operaciones se aplican transaccionalmente, de una forma que garantiza la integridad de los datos almacenados en la base de datos.

**Los sistemas OLTP aplican transacciones que admiten la denominada semántica ACID:**

1. ***Atomicidad:*** cada transacción se trata como una sola unidad, que se realiza correctamente o falla por completo. Por ejemplo, una transacción que conlleve el adeudo de fondos de una cuenta y el abono de la misma cantidad en otra debe completar ambas acciones. Si alguna de las acciones no se puede completar, se debe producir un error en la otra.
2. ***Coherencia:*** las transacciones solo pueden tomar los datos de la base de datos de un estado válido a otro. Para continuar con el ejemplo anterior del adeudo y el abono, el estado completado de la transacción debe reflejar la transferencia de fondos de una cuenta a la otra.
3. ***Aislamiento:*** las transacciones simultáneas no pueden interferir entre sí y deben dar lugar a un estado de base de datos coherente. Por ejemplo, mientras que la transacción para transferir fondos de una cuenta a otra está en proceso, otra transacción que comprueba el saldo de estas cuentas debe devolver resultados coherentes: la transacción de comprobación de saldo no puede recuperar un valor para una cuenta que refleje el saldo antes de la transferencia y un valor para la otra cuenta que refleje el saldo después de la transferencia.
4. ***Durabilidad:*** cuando se ha confirmado una transacción, permanece confirmada. Una vez completada la transacción de transferencia de cuenta, los saldos revisados de la cuenta se conservan para que incluso si el sistema de base de datos estuviera desactivado, la transacción confirmada se reflejará cuando se vuelva a activar.

Normalmente, los sistemas OLTP se usan para admitir aplicaciones activas que procesan datos empresariales, a menudo denominadas aplicaciones de línea de negocio (LOB).

**Procesamiento de datos analíticos**
El procesamiento analítico de datos suele utilizar sistemas de solo lectura (o de lectura casi exclusiva) que almacenan grandes volúmenes de datos históricos o métricas de negocio. Los análisis pueden basarse en una instantánea de los datos en un momento concreto o en una serie de instantáneas.

Una arquitectura común para el análisis a escala empresarial tiene el siguiente aspecto:

1. Los datos operativos se extraen, transforman y cargan (ETL) en un lago de datos para su análisis, o bien se extraen y cargan primero, y se transforman después, un patrón llamado ELT habitual en los lakehouses modernos.
2. Los datos se cargan en un esquema de tablas, normalmente en un almacén de lago de datos con abstracciones tabulares sobre archivos en el lago de datos, o un almacenamiento de datos con un motor SQL totalmente relacional.
3. Los datos del almacenamiento de datos se pueden agregar y cargar en un **modelo de procesamiento analítico en línea (OLAP)**, que actualmente se denomina más comúnmente un modelo semántico (e históricamente un cubo). Los valores numéricos agregados (medidas) de las tablas de hechos se calculan para intersecciones de dimensiones a partir de tablas de dimensiones. Por ejemplo, los ingresos de ventas podrían sumarse por fecha, cliente y producto. Los modelos semánticos de Power BI son un ejemplo común.
4. Los datos del lago de datos, el almacenamiento de datos y el modelo analítico se pueden consultar para generar informes, visualizaciones y paneles.

***Característica         Procesamiento transaccional (OLTP)                        Procesamiento analítico (OLAP)***

*Objetivo         Registrar operaciones diarias.                                Analizar datos y apoyar decisiones.*

*Operaciones         Crear, consultar, actualizar y eliminar registros (CRUD)       Consultar, comparar y resumir grandes volúmenes de datos.*

*Datos                 Actuales y detallados.                                        Históricos, acumulados y agregados.*

*Frecuencia         Continua, con cada operación.                                Periódica o según la necesidad de análisis.*

*Consultas         Cortas y específicas.                                        Complejas y sobre muchos registros.*

*Usuarios         Cajeros, vendedores y personal operativo.                Analistas, científicos de datos y gerentes.*

*Sistemas típicos        Bases de datos operativas.                                Data Warehouse, Data Lakehouse y modelos OLAP.*

*Ejemplo en una farmacia Registrar una venta y descontar inventario.                Comparar las ventas de 61 sucursales durante seis meses.*

En una frase: OLTP registra lo que sucede en el negocio; OLAP analiza los datos para decidir qué hacer.

**Organización de datos con la arquitectura medallón**
Un patrón común para organizar los datos en un lakehouse es la arquitectura de medallón, que utiliza tres capas:

1. Bronze: datos sin procesar ingeridos as-is de los sistemas de origen, sin ninguna transformación aplicada, conservando los registros originales para el reprocesamiento.

2\. Silver: datos limpios y conformes, con duplicados eliminados y tipos de datos estandarizados.

3\. Gold: datos agregados y listos para la empresa modelados para casos de uso específicos de informes y análisis.

**Característica Lago de datos (Data Lake)         Almacén de datos (Data Warehouse)                            Lago de datos híbrido (Data Lakehouse)**
Objetivo Almacenar grandes volúmenes de datos. Organizar datos para el análisis y la elaboración de informes.    Combinar almacenamiento flexible con

&#x20;                                                                                                                          capacidades de análisis.

Tipos de datos Estructurados, semiestructurados  Principalmente datos estructurados.                            Datos de distintos formatos,

&#x20;               y no estructurados.                                                                                        incluidos datos estructurados.

Almacenamiento Archivos en diferentes formatos. Tablas organizadas en un sistema de almacenamiento analítico.    Archivos y tablas con funciones de gestión

&#x20;                                                                                                                          de datos.

Preparación     Puede guardar datos originales          Generalmente requiere preparar y transformar los datos.            Permite almacenar datos originales y

&#x20;de datos       sin transformar.                                                                                           preparar tablas para análisis.

Consultas Dependen de las herramientas          Optimizadas para consultas analíticas mediante SQL.            Permite realizar consultas analíticas sobre

&#x20;               utilizadas para acceder a los datos.                                                                       tablas y archivos gestionados.

Calidad y  Dependen de los procesos y          Suele aplicar esquemas y controles para mantener             Puede incorporar transacciones, control de

confiabilidad   herramientas implementados.             la consistencia.                                                   versiones y otros controles de confiabilidad.

Usuarios  Ingenieros y científicos de datos. Analistas de datos y usuarios empresariales.                    Ingenieros, científicos, analistas y

principales                                                                                                                usuarios empresariales.

Ventaja  Flexibilidad para almacenar muchos  Consultas e informes empresariales organizados.                    Flexibilidad junto con capacidades de

principal       tipos de datos.                                                                                            gestión y análisis.

Ejemplo de uso Guardar archivos de ventas,          Analizar ventas, ingresos y márgenes por sucursal.            Guardar grandes volúmenes de datos y

&#x20;               registros de aplicaciones e imágenes.                                                                      analizarlos mediante tablas confiables.
