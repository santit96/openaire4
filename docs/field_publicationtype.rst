.. _aire:resourceType:

Resource Type (Tipo de recurso) (M)  
===================================

``oaire:resourceType``

Definición y alcance del campo
------------------------------

Este campo tiene varios usos dependiendo del contexto general de aplicación, los distintos usos se enumeran a continuación:

	- **Tipología Documental Normalizada COAR (M,1):** Hace referencia al tipo de publicación basándose en un vocabulario controlado normalizado, el cual es utilizado por el usuario (una máquina) para identificar la categoría asociada al recurso que está mostrando.

	- **Tipología Documental Normalizada RedCol (MA,1):** Hace referencia al tipo de recurso de investigación reconocido y avalado por Colciencias basándose en un vocabulario controlado normalizado, el cual es utilizado por el usuario (una máquina) para identificar la categoría asociada al recurso que está mostrando.

	- **Tipología Documental Local (R,1):** Hace referencia al tipo de producción científica o contenido intelectual en el que se manifiesta el recurso, el cual es utilizado por el usuario (una persona) para identificar la categoría asociada al recurso que está mostrando.  Ejemplo: Libro, artículo, revista, etc. 

	- **Tipología del Contenido del Recurso (O,1):** Hace referencia al tipo de contenido interno sobre el cual está construido el documento basándose en un vocabulario controlado normalizado. 

Niveles de persistencia (M/MA/R/O)
------------------------------------

	- Tipología Documental Normalizada COAR: Obligatorio (M,1)
	- Tipología Documental Normalizada RedCol: Obligatorio si es aplicable (MA,1)
	- Tipología Documental Local: Recomendado (R,1)
	- Tipología del Contenido del Recurso: Opcional (O,1)


Niveles de ocurrencia (R / NR)
------------------------------
Repetible (R) según los distintos contextos de aplicación de la tipología documental asociada.

Esquema de metadatos
------------------------------
oaire:resourcetype 

Traducción al español
---------------------
Tipo de recurso / Tipología Documental / Tipología del Contenido

Forma de Descripción Normalizada (RDA / RCAA2/ ISBD)
----------------------------------------------------
RDA (Recursos: descripción y acceso)

	Revise la forma adecuada para seleccionar el tipo de recurso:

		- **Tipología Documental Local:** Texto libre. Sin embargo se recomienda utilizar un vocabulario controlado de tipologías documentales. Esta directriz sugiere un vocabulario asociado a este campo. 
		- **Tipología Documental Normalizada COAR:** Se debe seleccionar el tipo de recurso que debe estar debidamente relacionado con una uri definido con el vocabulario controlado de COAR.
		- **Tipología Documental Normalizada RedCol:** Se debe seleccionar el tipo de recurso que debe estar debidamente relacionado con una uri definido con el vocabulario controlado de REDCOL.
		- **Tipología del Contenido del Recurso:** Se debe seleccionar el tipo de contenido del recurso según vocabulario controlado provisto (resourceTypeGeneral).

Propiedades, atributos y especificadores de campo
-------------------------------------------------

Propiedad Tipo de Recurso (resourceType) (M/MA/O/R, 1-n):
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Utilice la etiqueta del término de tipo de recurso como valor. Utilice el **valor del atributo asociado a la tipología documental que es** utilizado por el **usuario (una persona)** para identificar la categoría que está describiendo. Se puede utilizar la etiqueta en cualquier idioma indicado en el vocabulario.

	- **Atributo: Tipo de Contenido General (resourceTypeGeneral) (MA, 1):** Este atributo permite especificar el tipo de contenido asociado a la tipología documental descrita del recurso de información. Se debe tener en cuenta los siguientes tipos de contenido y su codificación normalizada según el vocabulario controlado propuesto:
	  
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Vocabulario Normalizado | Descripción del Atributo                                                                                                                                                                                                         | Dominio de Vocabulario |
	+=========================+==================================================================================================================================================================================================================================+========================+
	| Audiovisual             | Contenido Audiovisual/Multimedia. Una serie de representaciones visuales que imparten una impresión de movimiento cuando se muestran en sucesión. Puede o no incluir sonido. En el Vocabulario DC se representa como MovingImage | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Collection              | Contenido Colección. Una agregación de recursos, que puede abarcar colecciones de un tipo de recurso así como de tipos mixtos. Una colección se describe como un grupo; Sus partes también se pueden describir por separado.     | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| DataPaper               | Contenido Publicación de datos. Una publicación especializada con la intención de identificar y describir datos específicos, conjuntos de datos o recopilaciones de datos para facilitar el descubrimiento.                      | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Dataset                 | Contenido Conjunto de datos. Datos codificados en una estructura definida.                                                                                                                                                       | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Event                   | Contenido Acontecimiento. Una ocurrencia no persistente, basada en el tiempo.                                                                                                                                                    | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Image                   | Contenido Imagen. Una representación visual que no sea texto. En el vocabulario DC se representa como Image, StillImage                                                                                                          | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| InteractiveResource     | Contenido Recurso interactivo. Un recurso que requiere la interacción del usuario para ser comprendido, ejecutado o experimentado.                                                                                               | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Model                   | Contenido Modelo. Un modelo abstracto, conceptual, gráfico, matemático o de visualización que representa objetos empíricos, fenómenos o procesos físicos.                                                                        | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| PhysicalObject          | Contenido Objeto físico. Un objeto o sustancia inanimada, tridimensional.                                                                                                                                                        | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Service                 | Contenido Servicio. Un sistema organizado de aparatos, aparatos, personal, etc., para suministrar algunas funciones requeridas por los usuarios finales.                                                                         | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Software                | Contenido Software. Un programa informático en código fuente (texto) o en forma compilada. Utilice este tipo de contenido para todos los componentes de software relacionados.                                                   | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Sound                   | Contenido Sonido. Un recurso destinado principalmente a ser escuchado.                                                                                                                                                           | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Text                    | Contenido Texto. Un recurso formado principalmente por palabras para la lectura.                                                                                                                                                 | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Workflow                | Contenido Flujo de Trabajo. Una serie estructurada de pasos que se pueden ejecutar para producir un resultado final, que permite a los usuarios especificar y ejecutar su trabajo de una manera más reproducible.                | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+
	| Other                   | Contenido Otros. Contenido que no se puede describir en los anteriores elementos.                                                                                                                                                | datacite               |
	+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+


	- **Atributo: Contexto de la Tipología (resourceTypeContext) (R, 1):** Este atributo permite especificar el contexto de uso de la tipología según los distintos usos y aplicaciones. En el evento que este atributo no sea declarado, se entenderá que la tipología suministrada se describe según vocabulario COAR. Se debe tener en cuenta los siguientes contextos y su codificación normalizada según el vocabulario controlado propuesto:
	
	+-------------------------+-------------------------------------------------------------------+------------------------+
	| Vocabulario Normalizado | Descripción del Atributo                                          | Dominio de Vocabulario |
	+=========================+===================================================================+========================+
	| coar                    | Tipología documental descrita según vocabulario COAR              | redcol                 |
	+-------------------------+-------------------------------------------------------------------+------------------------+
	| redcol                  | Tipología documental descrita según vocabulario REDCOL            | redcol                 |
	+-------------------------+-------------------------------------------------------------------+------------------------+
	| local                   | Tipología documental descrita según vocabulario LOCAL             | redcol                 |
	+-------------------------+-------------------------------------------------------------------+------------------------+
	| other                   | Otra categoría de de tipologías documentales asociadas al recurso | redcol                 |
	+-------------------------+-------------------------------------------------------------------+------------------------+

	- **Atributo: Identificador Uniforme del Recurso (uri) (M, 1):** Este atributo permite especificar un identificador semántico basado en un vocabulario controlado (ontología) para describir de manera unívoca una tipología documental.
	
		- **Tipología Documental Normalizada COAR:** Se debe seleccionar el tipo de recurso que debe estar debidamente relacionado con una uri definida con el vocabulario controlado de COAR:
		
**Vocabulario normalizado de Tipos Documentales OPENAIRE-COAR**

+-----------------------------------------------+-------------------------+
| ConceptURI                                    | Etiqueta                |
+===============================================+=========================+
| http://purl.org/coar/resource_type/c_1162     | Anotación               |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_6501     | Artículo de revista     |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_545b     | Carta al editor         |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_b239     | Editorial               |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_2df8fbb1 | Artículo de             |
|                                               | investigación           |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_dcae04bc | Artículo de revisión    |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_beb9     | Papel de datos          |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_3e5a     | Contribución a la       |
|                                               | revista                 |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_ba08     | Reseña de libro         |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_3248     | Parte de libro          |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_2f33     | Libro                   |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_86bc     | Bibliografía            |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_816b     | Preimpresión            |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_8042     | Documento de trabajo    |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_71bd     | Documentación técnica   |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18gh     | Reporte técnico         |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18ws     | Informe de investigación|
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18hj     | Informe agencia de      |
|                                               | financiamiento          |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18op     | Entregable de proyecto  |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_186u     | Informe de política     |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18wq     | Otro tipo de informe    |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18wz     | Memorando               |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18ww     | Informe interno         |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_efa0     | Revisión                |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_baaf     | Propuesta de            |
|                                               | investigación           |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_ba1f     | Parte del informe       |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_93fc     | Informe                 |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_15cd     | Patente                 |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18co     | Documento de conferencia|
|                                               | en proceso              |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18cp     | Documento de conferencia|
|                                               | en no proceso           |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_6670     | Póster de la conferencia|
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_5794     | Documento de sesión     |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_c94f     | Objeto de conferencia   |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_f744     | Actas de conferencia    |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_7a1f     | Trabajo de grado de     |
|                                               | pregrado                |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_bdcc     | Tesis de maestría       |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_db06     | Tesis doctoral          |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_46ec     | Tesis                   |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_0857     | Carta                   |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_8544     | Conferencia             |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18cf     | Texto                   |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18cw     | Notación musical        |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18cd     | Composición musical     |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_18cc     | Sonido                  |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_12ce     | Video                   |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_8a7e     | Imagen en movimiento    |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_ecc8     | Imagen fija             |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_c513     | Imagen                  |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_12cd     | Mapa                    |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_12cc     | Material cartográfico   |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_5ce6     | Software                |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_ddb1     | Conjunto de datos       |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_e9a0     | Recurso interactivo     |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_7ad9     | Sitio web               |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_393c     | Flujo de trabajo        |
+-----------------------------------------------+-------------------------+
| http://purl.org/coar/resource_type/c_1843     | Otro                    |
+-----------------------------------------------+-------------------------+

- **Tipología Documental Normalizada RedCol:** Se debe seleccionar el tipo de recurso que debe estar debidamente relacionado con una uri definida con el vocabulario controlado de REDCOL:

**Productos resultados de actividades de generación de nuevo conocimiento**

+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Tipo Documental Específico Colciencias                        | Notas                                                                                                                              | Valor Autorizado                              |
+===============================================================+====================================================================================================================================+===============================================+
| Artículos de investigación                                    | Campo ya descrito en Vocabulario COAR/OPENAIRE. http://purl.org/coar/resource_type/c_2f33                                          |                                               |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Notas Científicas                                             |                                                                                                                                    | https://purl.org/redcol/resource_type/N       |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Libros resultado de investigación                             | Campo ya descrito en Vocabulario COAR/OPENAIRE                                                                                     | https://purl.org/redcol/resource_type/LIB     |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Capítulos en libro resultado de investigación                 | Campo ya descrito en Vocabulario COAR                                                                                              | https://purl.org/redcol/resource_type/CAP_LIB |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Patente de invención                                          | Selecionar del Vocabulario COAR/OPENAIRE “Patente” y utilizar el siguiente elemento semántico para especificar el tipo de Patente: | https://purl.org/redcol/resource_type/PA      |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Patente de modelo de utilidad                                 | Selecionar del Vocabulario COAR/OPENAIRE “Patente” y utilizar el siguiente elemento semántico para especificar el tipo de Patente: | https://purl.org/redcol/resource_type/MA      |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Variedad vegetal                                              |                                                                                                                                    | https://purl.org/redcol/resource_type/VV      |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Variedad animal                                               |                                                                                                                                    |                                               |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Nueva raza animal                                             |                                                                                                                                    | https://purl.org/redcol/resource_type/VA      |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Poblaciones mejoradas de razas pecuarias                      |                                                                                                                                    | https://purl.org/redcol/resource_type/VA_B    |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Obras o Productos de creación en artes, arquitectura y diseño |                                                                                                                                    | https://purl.org/redcol/resource_type/AAD     |
+---------------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+


**Productos resultados de actividades de desarrollo tecnológico e innovación**

..


.. tabularcolumns:: |\Y{0.3}|\Y{0.3}|\Y{0.4}|

+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Tipo Documental Específico Colciencias                                           | Notas                        | Valor Autorizado                            |
+==================================================================================+==============================+=============================================+
|                                **Productos Tecnológicos Certificados o Validados**                                                                            |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Diseño industrial                                                                |                              | https://purl.org/redcol/resource_type/DI    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Esquema de trazado de circuito integrado                                         |                              | https://purl.org/redcol/resource_type/ECI   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Software                                                                         |                              | https://purl.org/redcol/resource_type/SF    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Planta piloto                                                                    |                              | https://purl.org/redcol/resource_type/PP    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Prototipo industrial                                                             |                              | https://purl.org/redcol/resource_type/PI    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Signos distintivos                                                               |                              | https://purl.org/redcol/resource_type/SD    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Productos nutraceúticos                                                          |                              | https://purl.org/redcol/resource_type/PN    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Colección científica                                                             |                              | https://purl.org/redcol/resource_type/CC    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Nuevo registro científico                                                        |                              | https://purl.org/redcol/resource_type/NRC   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
|                                    **Productos Empresariales**                                                                                                |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Secreto empresarial                                                              |                              | https://purl.org/redcol/resource_type/SE    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Empresas de base tecnológica (Spin-off y Start-up)                               |                              | https://purl.org/redcol/resource_type/EBT   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Empresas creativas y culturales                                                  |                              | https://purl.org/redcol/resource_type/ICC   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Innovación generada en la gestión empresarial                                    |                              | https://purl.org/redcol/resource_type/IG    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Innovación en procedimiento y servicio                                           |                              | https://purl.org/redcol/resource_type/IPP   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
|                                    **Regulación Norma o Reglamento**                                                                                          |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Regulación Norma o Reglamento                                                    |                              | https://purl.org/redcol/resource_type/RNT   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Guía de Práctica Clínica                                                         |                              | https://purl.org/redcol/resource_type/RNP   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Guía de Manejo Clínico Forense                                                   |                              | https://purl.org/redcol/resource_type/GMCF  |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Manuales y Modelos de atención diferencial a víctimas                            |                              | https://purl.org/redcol/resource_type/MADV  |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Protocolos de atención a usuarios                                                |                              | https://purl.org/redcol/resource_type/PAU   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Protocolo de Vigilancia Epidemiológica (PVE)                                     |                              | https://purl.org/redcol/resource_type/PVE   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Acto legislativo                                                                 |                              | https://purl.org/redcol/resource_type/AL    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Proyecto de Ley                                                                  |                              | https://purl.org/redcol/resource_type/RNPL  |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
|                                      **Conceptos técnicos**                                                                                                   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Conceptos técnicos                                                               |                              | https://purl.org/redcol/resource_type/CT    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Informe final de investigación                                                   |                              | https://purl.org/redcol/resource_type/INF   |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+
| Acuerdo de licencia para la explotación de obras protegidas por derecho de autor |                              | https://purl.org/redcol/resource_type/MR    |
+----------------------------------------------------------------------------------+------------------------------+---------------------------------------------+

..

**Productos resultados de actividades de apropiación social del conocimiento**

.. tabularcolumns:: |\Y{0.3}|\Y{0.3}|\Y{0.4}|

+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Tipo Documental Específico Colciencias                                           | Notas                    | Valor Autorizado                                |
+==================================================================================+==========================+=================================================+
| Participación ciudadana en proyectos de CTI                                      |                          | https://purl.org/redcol/resource_type/PPC       |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Espacios de participación ciudadana en CTI                                       |                          | https://purl.org/redcol/resource_type/EPC       |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Estrategia pedagógicas para el fomento a la CTI                                  |                          | https://purl.org/redcol/resource_type/EPA       |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Estrategia de comunicación del conocimiento                                      |                          | https://purl.org/redcol/resource_type/PPK       |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Generación de contenido                                                          |                          | https://purl.org/redcol/resource_type/GC        |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Evento científico                                                                |                          | https://purl.org/redcol/resource_type/EC        |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Red de conocimiento especializado                                                |                          | https://purl.org/redcol/resource_type/RC        |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Taller de Creación                                                               |                          | https://purl.org/redcol/resource_type/TC        |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Eventos culturales y artísticos                                                  |                          | https://purl.org/redcol/resource_type/ECA       |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Documento de trabajo                                                             |                          | https://purl.org/redcol/resource_type/WP        |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Nueva Secuencia Genética                                                         |                          | https://purl.org/redcol/resource_type/NSG       |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Boletín divulgativo de resultado de investigación                                |                          | https://purl.org/redcol/resource_type/BOL       |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Edición                                                                          |                          | https://purl.org/redcol/resource_type/ERL       |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Informe de investigación                                                         |                          | https://purl.org/redcol/resource_type/IFI       |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Consultoría científicas-tecnologías                                              |                          | https://purl.org/redcol/resource_type/CON_CT    |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+
| Consultoría de procesos en investigación-creación en arte, arquitectura y diseño |                          | https://purl.org/redcol/resource_type/CON_AAD   |
+----------------------------------------------------------------------------------+--------------------------+-------------------------------------------------+


..

**Productos de actividades relacionadas con la Formación de Recurso Humano en CTeI**

+-------------------------------------------------------+------------------------------------------+-------------------------------------------+
| Dirección de Tesis de doctorado                       |                                          | https://purl.org/redcol/resource_type/TD  |
+-------------------------------------------------------+------------------------------------------+-------------------------------------------+
| Dirección de Trabajo de grado de maestría             |                                          | https://purl.org/redcol/resource_type/TM  |
+-------------------------------------------------------+------------------------------------------+-------------------------------------------+
| Dirección de Trabajos de grado de pregrado            |                                          | https://purl.org/redcol/resource_type/TP  |
+-------------------------------------------------------+------------------------------------------+-------------------------------------------+
| Proyecto de investigación y Desarrollo                |                                          | https://purl.org/redcol/resource_type/PID |
+-------------------------------------------------------+------------------------------------------+-------------------------------------------+
| Proyecto de investigación-Creación                    |                                          | https://purl.org/redcol/resource_type/PIC |
+-------------------------------------------------------+------------------------------------------+-------------------------------------------+
| Proyecto de extensión y responsabilidad social en CTI |                                          | https://purl.org/redcol/resource_type/PE  |
+-------------------------------------------------------+------------------------------------------+-------------------------------------------+
| Apoyo creación de cursos                              |                                          | https://purl.org/redcol/resource_type/AP  |
+-------------------------------------------------------+------------------------------------------+-------------------------------------------+
| Asesoría al programa Ondas                            |                                          | https://purl.org/redcol/resource_type/APO |
+-------------------------------------------------------+------------------------------------------+-------------------------------------------+

..

- **Tipología Documental Local:** Texto libre. Se sugiere utilizar este atributo como elemento regional/local asociado a la descripción de la tipología documental que indica el texto de despliegue al usuario final (humano). Con el fin de regular la cantidad de tipología documentales locales, se recomienda crear un listado ó vocabulario controlado de tipologías documentales. Se provee un ejemplo de vocabulario de tipologías documentales:

..

+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| Item | COLECCIÓN                              | TIPOLOGÍAS DOCUMENTALES                             | NOTAS                                                        |
+======+========================================+=====================================================+==============================================================+
| 1    | Libros                                 | Libro completo                                      |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Capítulo de libro                                   |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 2    | Documentos                             | Documento de trabajo                                |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Ensayo                                              |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Informe de investigación                            |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Manual                                              |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Plan de trabajo                                     |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Propuesta de investigación                          |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Trabajo docente                                     |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Documento Legal - Jurisprudencia                    |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Documento Histórico                                 |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Literatura Gris                                     |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Patente                                             |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Reporte                                             |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Licencia                                            |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 3    | Periódicas y/o seriadas                | Artículo de periódico                               |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Artículo de revista                                 |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Balance de gestión                                  |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Boletín                                             |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Censo                                               |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Documento de Conferencia                            | Incluye, Poster, resumen, memorias y programa de conferencia |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Diagnóstico                                         |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Informe de gestión                                  |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Periódico                                           |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Revista                                             |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 4    | Tesis y trabajos de grado              | Tesis/Trabajo de grado - Monografía - Pregrado      |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Tesis/Trabajo de grado - Monografía -               |                                                              |
|      |                                        | Especialización                                     |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Tesis/Trabajo de grado - Monografía - Maestría      |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Tesis/Trabajo de grado - Monografía - Doctorado     |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Tesis/Trabajo de grado - Monografía - PosDoctorado  |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 5    | Videograbaciones y grabaciones sonoras | Grabaciones sonoras                                 |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Audio                                               |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Multimedia                                          |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Videograbación                                      |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 6    | Imágenes y Fotografías                 | Fotografías                                         |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Imágenes                                            |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 7    | Mapas                                  | Mapa                                                |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Punto Geográfico                                    |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 8    | Objetos de aprendizaje                 | Recurso Educativo Digital Abierto REDA              |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Curso                                               |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | MOOC                                                |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 9    | Referencias bibliográficas             | Referencia bibliográfica                            |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Entrada de diccionario                              | Concepto, definición, entrada de enciclopedia.               |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 10   | Software                               | Aplicativo                                          |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Juego                                               |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Simulación                                          |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
|      |                                        | Sitio Web                                           |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+
| 11   | Datos                                  | Datos - colección de datos                          |                                                              |
+------+----------------------------------------+-----------------------------------------------------+--------------------------------------------------------------+


Relaciones con otros campos
---------------------------

- No confundir con el campo Formato (R), porque hace referencia al tipo de medio en el que está el recurso. 

Restricciones
-------------

Ninguna


Ejemplos y ayudas
-----------------

**Esquema oai_dc**

.. code-block:: xml
   :linenos:

   <dc:type>Trabajo de grado - Pregrado</dc:type>
   <dc:type>Text</dc:type>
   <dc:type>http://purl.org/coar/resource_type/c_7a1f</dc:type>
   <dc:type>https://purl.org/redcol/resource_type/TP</dc:type>


**Esquema DataCite**

.. code-block:: xml
   :linenos:

   <oaire:resourceType resourceTypeGeneral="literature" resourceTypeContext="coar" uri="http://purl.org/coar/resource_type/c_6501">journal article</oaire:resourceType>

**Esquema xaoi**

.. code-block:: xml
   :linenos:

   <element name="type">
   <element name="es_ES">
     <field name="value">http://purl.org/coar/resource_type/c_7a1f</field>
   </element>
	</element>

**Esquema dim**

.. code-block:: xml
   :linenos:

   <dim:field mdschema="dc" element="type" lang="es_ES">http://purl.org/coar/resource_type/c_7a1f</dim:field>


Niveles de aplicación para productos de investigación de Colciencias
--------------------------------------------------------------------
REDCOL ha desarrollado el siguiente vocabulario controlado acorde con los productos de investigación reconocidos y avalados por Colciencias y que se ciñe a los modelos semánticos provistos por DATACITE y OPENAIRE.  

Los sistemas de información deben utilizar estos nuevos elementos para describir tipologías documentales que no se encuentran descritas en el **Vocabulario normalizado de Tipos Documentales OPENAIRE-COAR.** En este contexto, para describir estos tipos documentales asociados a los productos específicos de Colciencias,  para el campo anterior  se debe utilizar  el valor “other - http://purl.org/coar/resource_type/c_1843”  y posteriomente seleccionar el tipo documental específico del vocabulario.


Relaciones con otros modelos de metadatos
-----------------------------------------
El campo **Tipo de recurso (oaire:resourcetype)** es utilizado por los siguientes esquemas:

+----------------------+-----------------------+
| Esquema de Metadatos | Campo Relacionado     |
+======================+=======================+
| marcxml              | 008 Posición 24       |
+----------------------+-----------------------+
| dc                   | dc.type               |
+----------------------+-----------------------+
| dcterms              | dcterms.type          |
+----------------------+-----------------------+
| datacite             | datacite.resourcetype |
+----------------------+-----------------------+



Niveles semánticos
------------------

Los campos de los atributos de los vocabularios controlados están construidos en skos por la confederación de repositorio de acceso abierto COAR. (https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/)

Recomendación de campos de aplicación en DSPACE
-----------------------------------------------

Se recomienda crear/modificar el componente de registro de metadatos (y sus correspondientes hojas de entrada de datos) de los sistemas DSPACE basados en los siguientes elementos:


===================================================  =======================  ====================  ==============================================================================================================
Vocabulario controlado OpenAire/RedCol               Campo Elemento DSPACE    Calificadores         Nota de alcance                                                                                               
===================================================  =======================  ====================  ==============================================================================================================
Tipología Documental Normalizada COAR                dc.type                  coar                  Incluir la URI                                                                                                
Tipología Documental Normalizada Drive/OpenAireV3    dc.type                  driver                Campo Obsoleto, utilizar únicamente con fines de compatibilidad con versiones anteriores                      
Tipología Documental Normalizada RedCol              dc.type dc.type          redcol colciencias    Incluir la URI NOTA: Se presenta equivalencia semántica para los campos dc.type.redcol y dc.type.colciencias  
Tipología Documental Normalizada Local               dc.type dc.type          local                 Incluir el Texto para Usuarios. NOTA:
																									* Se presenta equivalencia semántica para los campos dc.type y dc.type.local
																									* Para este campo se recomienda utilizar el vocabulario propuesto para tipología documental local                                                                         
Tipología del Contenido del Recurso                  dc.type                  content               Utilizar vocabulario controlado                                                                               
===================================================  =======================  ====================  ==============================================================================================================


Recomendaciones de migración de otras directrices de metadatos (BDCOL, SNAAC, LA REFERENCIA, OPENAIRE 2, OPENAIRE 3)
--------------------------------------------------------------------------------------------------------------------

- Las versiones anteriores de las Directrices de OpenAIRE y Driver utilizaban el vocabulario info: eu-repo para los tipos de publicación.
  
+-----------+-------------------------------------------------+------------+
| Tipología | Driver/OpenaireV3                               | OpenAireV4 |
+===========+=================================================+============+
|           | info:eu-repo/semantics/article                  |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/bachelorThesis           |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/masterThesis             |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/doctoralThesis           |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/book                     |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/bookPart                 |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/review                   |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/conferenceObject         |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/lecture                  |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/workingPaper             |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/preprint                 |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/report                   |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/annotation               |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/contributionToPeriodical |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/patent                   |            |
+-----------+-------------------------------------------------+------------+
|           | info:eu-repo/semantics/other                    |            |
+-----------+-------------------------------------------------+------------+


- Este conjunto de directrices está utilizando el elemento **resourceType** del esquema de metadatos DataCite MetadataKernel v4.2.
- A dicho esquema se le adicionaron dos atributos para refinar el contenido del campo:
  
  - El atributo **uri** para el concepto de tipo de recurso URI a este perfil de aplicación
  - El atributo **resourceTypeContext** para determinar el contexto de aplicación de la tipología documental descrita.

