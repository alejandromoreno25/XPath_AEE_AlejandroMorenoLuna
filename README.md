# Reto de Refactorización. TechNova Cloud v2.0

**¿Cuántas líneas de código habéis ahorrado al usar grupos?**

Al utilizar attributeGroup para los atributos del servidor y group para el bloque de hardware, hemos ahorrado aproximadamente unas 20 lineas que aunque no parezca mucho al ser muy pequeño este codigo, puede llegar a ser muy difcerencial o bastante en proyectos a gran Escala. Por ello, 
la capacidad de reutilizar estos bloques evita errores de escritura y reduce el tamaño del archivo XSD considerablemente.

**¿Qué error os da VS Code si intentáis poner dos servidores con el mismo ID?**

Gracias a la restricción unique, VS Code me da un eror así: 
Identity constraint error: 'UnicoID' has found a duplicate key
Esto sucede porque el validador ahora no solo mira que el formato sea correcto, sino que ahora rastrea todo el xsd buscando esas restricciones.
