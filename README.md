# BOM Toolbox Analyzer

El **BOM Toolbox Analyzer** es una herramienta de ingeniería de precisión diseñada para facilitar la gestión, auditoría y optimización de Listas de Materiales (BOM) en el desarrollo de hardware electrónico. Su objetivo principal es transformar datos brutos en insights accionables que permitan reducir costes y estandarizar componentes desde la fase de diseño.

## ¿Para qué sirve?

Esta herramienta permite a ingenieros de hardware, gestores de compras y especialistas en *Product Costing* visualizar la estructura de costes de un proyecto de manera intuitiva. Ayuda a identificar rápidamente qué subsistemas, componentes o tipos de encapsulados están impactando negativamente en el presupuesto del producto (inversor o placa electrónica), facilitando la toma de decisiones basada en datos.

## Funcionalidades Principales

* **Análisis DTC (Design to Cost) Automatizado:** Identifica automáticamente oportunidades de ahorro, como componentes con tolerancias excesivamente estrictas o diversidad innecesaria de encapsulados.
* **Gestión Dinámica de BOM:** Permite cargar archivos CSV, excluir componentes específicos y realizar simulaciones *What-If* editando los precios unitarios en tiempo real para ver el impacto inmediato en el coste final.
* **Visualización de Costes:** Genera gráficos interactivos para analizar la distribución de costes por Módulos, Submódulos y una **Curva de Pareto** (análisis 80/20) para priorizar los esfuerzos de optimización sobre los componentes de mayor impacto económico.
* **Filtros Jerárquicos:** Herramientas integradas para filtrar el análisis por secciones específicas del diseño, facilitando auditorías granulares.
* **Integración con Suministro:** Enlaces directos a buscadores de componentes para verificar disponibilidad y precios de mercado de los *Part Numbers* (MPNs) cargados.

## Casos de Uso

1.  **Auditoría de Costes de Proyecto:** Identificar rápidamente los "cost drivers" o componentes que consumen la mayor parte del presupuesto en placas complejas.
2.  **Estandarización de Inventario:** Reducir la diversidad de componentes (ej. resistencias y condensadores) unificando valores y encapsulados para simplificar la cadena de suministro y el proceso de montaje en planta (*Pick-and-Place*).
3.  **Optimización de Diseño (DTC):** Evaluar si el uso de componentes de alta precisión (ej. tolerancias <1% o dieléctricos costosos como C0G/NP0) es realmente necesario para cada subsistema, sugiriendo alternativas más comerciales.
4.  **Preparación de RFQ (Request for Quotation):** Limpiar y preparar listas de materiales optimizadas antes de enviarlas a fabricantes por contrato.

## Formato de Importación

Para asegurar un funcionamiento correcto, el archivo CSV debe contener las siguientes columnas (se aceptan variaciones en los nombres de las cabeceras):
* `Designator`
* `Description`
* `Quantity`
* `Manufacturer`
* `PartNumber`
* `Unit Price`
* `Total Price`
* `Modulo`
* `SubModulo`

*Nota: La aplicación procesa los cálculos localmente en su navegador, garantizando la privacidad de los datos de su BOM.*
