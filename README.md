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
