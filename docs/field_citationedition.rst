.. _aire:citationEdition:

Citation Edition (Edición del recurso fuente) (R)
=================================================

``oaire:citationEdition``

Definición y alcance del campo
------------------------------
Este campo hace referencia a la designación numérica/secuencial de la edición del recurso fuente. Esta propiedad es parte de la cita bibliográfica.

Niveles de persistencia (M/MA/R/O)
----------------------------------
Recomendado (R) 

Niveles de ocurrencia (R / NR)
------------------------------
No repetible (NR): 0-1


Esquema de metadatos
--------------------
oaire:citationEdition

Traducción al español
---------------------
Edición del recurso fuente

Forma de Descripción Normalizada (RDA/RCAA2/ISBD)
-------------------------------------------------
RDA (Recursos: descripción y acceso): Revise la forma adecuada para ingresar el número de edición del recurso de información fuente (enfocado especialmente para recursos monográficos).

Propiedades, atributos y especificadores de campo
-------------------------------------------------

Propiedad Principal Ejemplar del recurso fuente (citationEdition) (R, 0-1): 
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Utilice el número de la edición como valor.

Relaciones con otros campos
---------------------------
El campo edición del recurso fuente **(oaire:citationEdition)** complementa la información del campo Título del recurso fuente **(oaire:citationTitle)** para tipologías documentales monográficas que utilicen este valor (principalmente - Libros)

Restricciones
-------------
No aplica

Ejemplos y ayudas
-----------------

Ayudas
++++++

Ejemplo en XML (Interoperabilidad OAI-PMH)
++++++++++++++++++++++++++++++++++++++++++

**Esquema oai_dc**

.. code-block:: xml
   :linenos:

   <dc:relation>16</dc:relation>

**Esquema DataCite**

.. code-block:: xml
   :linenos:

   <oaire:citationEdition>1</oaire:citationEdition>

**Esquema xoai**

.. code-block:: xml
   :linenos:

   <element name="relation">
     <element name="citationEdition">
     <element name="spa">
        <field name="value">4</field>
     </element>
   </element>
   </element>


**Esquema dim**

.. code-block:: xml
   :linenos:

   <dim:field mdschema="dc" element="relation" qualifier="citationEdition" lang="spa">5</dim:field>

.. code-block:: xml
   :linenos:

   <dim:field mdschema="oaire" element="citationEdition" qualifier="" lang="spa">5</dim:field>


Niveles de aplicación para productos de investigación de Colciencias
--------------------------------------------------------------------
Se aplica exclusivamente a todos los productos de Colciencias que utilicen edición de publicación.

Relaciones con otros modelos de metadatos
-----------------------------------------

El campo edición de publicación del recurso de información fuente **(oaire:citationEdition)** es utilizado por los siguientes esquemas de metadatos y puede intercambiarse su uso de manera indistinta mientras se conserven sus distintos niveles de atributos y especificadores de campo:

======================  ===================
Esquema de Metadatos    Campo Relacionado  
======================  ===================
marcxml                 field:250          
======================  ===================

Niveles semánticos
------------------
No aplica

Recomendación de campos de aplicación en DSPACE
-----------------------------------------------

Se recomienda crear/modificar el componente de registro de metadatos (y sus correspondientes hojas de entrada de datos) de los sistemas DSPACE basados en los siguientes elementos:

+----------------------------------------+-----------------------+---------------------------+------------------------------------------------------------------------------------------------------------+
| Vocabulario controlado OpenAire/RedCol | Campo Elemento DSPACE | Calificadores             | Nota de alcance                                                                                            |
+========================================+=======================+===========================+============================================================================================================+
| OpenAire                               | dc.relation           | citationedition - edition | Número de edición de publicación. Se pueden utilizar cualquiera de los dos esquemas provistos (dc, oaire). |
+----------------------------------------+-----------------------+---------------------------+------------------------------------------------------------------------------------------------------------+
| OpenAire                               | dc.description        | edition                   | Número de edición de publicación. Se pueden utilizar cualquiera de los dos esquemas provistos (dc, oaire). |
+----------------------------------------+-----------------------+---------------------------+------------------------------------------------------------------------------------------------------------+
| OpenAire                               | oaire                 | citationEdition           | Número de edición de publicación. Se pueden utilizar cualquiera de los dos esquemas provistos (dc, oaire). |
+----------------------------------------+-----------------------+---------------------------+------------------------------------------------------------------------------------------------------------+


Recomendaciones de migración de otras directrices de metadatos (BDCOL, SNAAC, LA REFERENCIA, OPENAIRE 2, OPENAIRE 3)
--------------------------------------------------------------------------------------------------------------------

- Se recomienda específicamente crear los nuevos atributos/especificadores de campo de **edición** según la codificación propuesta.