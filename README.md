# Lab06-prompts
# Bitacora de prompts 
Laboratorio 06: Fundamentos de Ingenieria de Prompts. 
Herramienta de IA usada: Gemini
## Ejercicio 2: Tokens y ventana de contexto 
| Texto | Caracteres | Tokens | 
|-------|------------|--------| 
| Los estudiantes programan en Java. | 7| 34| 
| The students program in Java. |6|29| 
| desafortunadamente |4| 18|


En el paso 4 pregunte le di un prompt estructurado y contexto de mi app y realice una pregunta sobre ese tema, en la pregunta 5 hice la misma pregunta y la IA no supo que responder.

## Ejercicio 3: Temperatura
| Temperatura | % de BiblioTec | Nombres en los 5 intentos | 
|-------------|----------------|---------------------------| 
| 0 |100% |  BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec| 
| 0.5 |65% | BiblioTec, BiblioTec, LibroYa, LibroYa, BiblioTec| 
| 1 | 44%| BiblioTec, BiblioTec, PrestaLibro, BiblioTec, LibroYa| 
| 1.8 |32% |LibroYa, NubeDeTinta, BiblioTec, BiblioTec, PrestaLibro |

Al aumentar la temperatura los nombres varían más porque la IA arriesga al elegir opciones menos probables.

## Ejercicio 4: Prompt vago vs estructurado 
| Criterio | Prompt vago | Prompt estructurado | 
|----------|-------------|---------------------|
| Menciona el objetivo del sistema | No|Si | 
| Menciona a los usuarios principales | No|Si | 
| Tiene exactamente 3 funcionalidades | No|Si | 
| Esta en 3 parrafos | No|Si | 
| Lo usaria en un informe real |No |Si |


## Ejercicio 5: Anatomia de un prompt 
| Componente | Texto de mi prompt | 
|------------|--------------------|
| Rol |Actua como desarrollador Java. |         
| Instruccion |Crea un programa en Java para gestionar los productos de  una tienda. | 
| Contexto |Para gestionar los productos de  una tienda. | 
| Ejemplo |Usando una clase Producto con los atributos codigo, nombre, precio y stock. | 
| Formato |Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |


## Ejercicio 6: Del prompt basico al profesional

```text 
(Actua como desarrollador Java. Crea un ejemplo de login para una 
aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.
Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.) 
```
Bitácora de ingeniería de prompts

# Tarea: Mi prompt profesional 
## Funcionalidad elegida 
## Version 1: prompt basico 
Genera una aplicacion en java
## Version 2 
Eres un ingeniero en sistemas, Genera una aplicacion en java profesional util para varios usuarios y que sea comercial
## Version 3: prompt final 
Actúa como Arquitecto de Software Senior con experiencia en apps de alto tráfico y comercio electrónico. Diseña la arquitectura de software end-to-end para una aplicación móvil híbrida (Social Network + Marketplace). Incluye: diagrama de componentes alto nivel, pila tecnológica justificada, modelo de datos simplificado, estrategia de escalabilidad, seguridad/pagos y patrones de diseño. Estructura la respuesta con formato técnico ejecutivo usando Markdown.

## Componentes del prompt final 

| Componente | Texto de mi prompt |
| :--- | :--- |
| **Rol** | Actúa como un Arquitecto de Software Senior con más de 10 años de experiencia en aplicaciones móviles de alto tráfico y e-commerce. |
| **Contexto** | Estoy diseñando desde cero una aplicación móvil comercial para iOS y Android que combina una red social de contenido visual (estilo Instagram) con un Marketplace en línea. |
| **Instrucción** | Diseña la arquitectura de software end-to-end completa y genera las especificaciones técnicas de alto nivel para este proyecto. |
| **Ejemplo** | Para la tabla de tecnologías usa esta estructura: Capa \| Tecnología \| Justificación (ej. Frontend Móvil \| Flutter \| Código base único para iOS/Android con renderizado nativo). |
| **Formato** | Estructura la respuesta en Markdown con: Diagrama de componentes en bloques ASCII, Tabla de Pila Tecnológica, Secciones explicativas para Módulos Core, Escalabilidad/Seguridad y Flujo de datos. |

## Evaluación del resultado

### 1. Criterios de Calidad
* **Claridad y Estructura:** La respuesta se entregó organizada con el formato solicitado (diagrama ASCII, tabla Markdown y secciones claras).
* **Precisión Técnica:** Las tecnologías sugeridas (como Flutter, PostgreSQL, Microservicios) son adecuadas para el nivel de complejidad del proyecto.
* **Cumplimiento de Instrucciones:** La IA respetó el rol de Arquitecto de Software y no incluyó código innecesario, enfocándose en el diseño de arquitectura.
### 2. Puntos Fuertes
* Separó correctamente la lógica de la red social de la lógica del Marketplace usando microservicios.
* Justificó de manera técnica cada herramienta elegida en la tabla de Tech Stack.
### 3. Oportunidades de Mejora / Ajustes
* *Ejemplo:* Se podría detallar más la parte de geolocalización o el algoritmo de recomendaciones para el feed.
### 4. Conclusión
El prompt estructurado logró que la IA generara una especificación técnica completa, profesional y directamente aplicable para la fase de diseño del software.

## Errores que evite
1. **Ambigüedad y vaguedad en la solicitud:**
   * *Error evitado:* Pedir algo genérico como *"Dime cómo hacer una app como Instagram"*, lo cual genera respuestas superficiales.
   * *Solución aplicada:* Definí un **Contexto** y una **Instrucción** claros especificando que es un híbrido entre Red Social y Marketplace.
2. **Falta de asignación de un Rol (Persona):**
   * *Error evitado:* Dejar que la IA responda de forma genérica o divulgativa.
   * *Solución aplicada:* Asigné el **Rol** de *Arquitecto de Software Senior*, obligando a la IA a adoptar un tono técnico, formal y especializado.
3. **Respuestas desestructuradas o difíciles de leer:**
   * *Error evitado:* Recibir un bloque de texto plano sin organización técnica.
   * *Solución aplicada:* Delimité el **Formato** exacto exigiendo diagramas en ASCII, tablas Markdown y secciones clasificadas.
4. **Malinterpretación del alcance del resultado (Ausencia de Few-Shot / Ejemplo):**
   * *Error evitado:* Que la IA entregara código fuente largo en lugar de un diseño de arquitectura.
   * *Solución aplicada:* Incluí un **Ejemplo** de la tabla deseada, guiando a la IA sobre la profundidad y estructura requerida.
5. **Omisión de restricciones clave:**
   * *Error evitado:* Que la IA asumiera tecnologías obsoletas o no justificara sus decisiones.
   * *Solución aplicada:* Forcé a la IA a incluir la columna de *Justificación Técnica* para validar el uso de cada herramienta.
