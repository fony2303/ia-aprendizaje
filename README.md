# Prompts reutilizables para gestión de un gimnasio

Primera pieza del portfolio del curso de IA generativa. Son cinco prompts, uno por tipo de tarea (redactar, analizar, resumir, planificar y revisar). Para cada uno incluyo la versión vaga, la versión mejorada y qué cambia entre ambas.

Los datos entre corchetes son marcadores: se sustituyen por los datos reales antes de usar el prompt.

## Índice

1. [Redactar: post de Instagram](#1-redactar-post-de-instagram)
2. [Analizar: KPI de trabajadoras](#2-analizar-kpi-de-trabajadoras)
3. [Resumir: reseñas de Google](#3-resumir-reseñas-de-google)
4. [Planificar: semana de clases especiales](#4-planificar-semana-de-clases-especiales)
5. [Revisar: oferta de coaching](#5-revisar-oferta-de-coaching)

---

## 1. Redactar: post de Instagram

**Versión vaga**

> Escribe un post para redes sobre mi gimnasio.

**Versión mejorada**

> Actúa como responsable de comunicación de Synergym Ourense Norte. Escribe un post de Instagram de 80 palabras anunciando estos tres eventos de noviembre:
> 1. Magic Circle, martes 10 de noviembre a las 9:30, con Liss
> 2. Step, miércoles 18 de noviembre a las 20:00, con Bea
> 3. Merengueton, lunes 23 de noviembre a las 10:30, con Liss
>
> Tono cercano, un emoji como máximo, menciona que se puede traer a un amigo y termina con una pregunta para comentar. No añadas datos que no te he dado.

**Qué cambia**

- El modelo tiene los datos del evento y no inventa nombres, fechas ni horarios.
- La longitud, el tono y el cierre están fijados.
- La prohibición de inventar protege lo que se publica.

**Prueba**

- **Versión vaga** (*"Escribe un post para redes sobre mi gimnasio."*): el post no menciona los eventos de noviembre y añade afirmaciones sobre instalaciones y atención que no se le dieron. Usa tres emojis, seis hashtags y no termina con una pregunta.
- **Versión mejorada:** anuncia los tres eventos con fecha, hora y trainer, usa un emoji, termina con una pregunta y no añade datos inventados. Cumple las 80 palabras aproximadas.
---

## 2. Analizar: KPI de trabajadoras

**Versión vaga**

> Revisa los KPI de mis trabajadoras y dime qué pueden mejorar.

**Versión mejorada**

> Actúa como responsable de operaciones de un gimnasio. Te pego a continuación una tabla con los datos de ventas y KPI de mis trabajadoras, del [fecha inicio] al [fecha fin], con las columnas: fecha, trabajadora, servicio, número de ventas, importe y [otros KPI].
>
> Haz lo siguiente:
> 1. Agrupa los datos por trabajadora y por servicio. Calcula totales y medias por trabajadora.
> 2. Compara a cada trabajadora con la media del equipo. Usa solo los datos de la tabla; si falta un dato, dilo y no lo estimes.
> 3. Para cada trabajadora, escribe dos listas: qué ha hecho bien y qué focos mejorar. Cada punto debe citar una cifra concreta.
>
> Formato: una tabla resumen y después una sección por trabajadora. Máximo 300 palabras por trabajadora.

**Qué cambia**

- El modelo conoce las columnas y el periodo, así que sabe qué calcular.
- Los pasos están numerados y se pueden comprobar uno a uno.
- Cada conclusión tiene una cifra, lo que facilita verificar el análisis.

**Prueba:** pendiente, con una tabla ficticia de 3 trabajadoras y 2 semanas.

---

## 3. Resumir: reseñas de Google

**Versión vaga**

> Resume las reseñas de Google de mi gimnasio y dime por qué se han quejado.

**Versión mejorada**

> Actúa como analista de experiencia de cliente de un gimnasio. Te pego a continuación [número] reseñas de Google del [fecha inicio] al [fecha fin], con su valoración.
>
> Haz lo siguiente:
> 1. Antes de nada, dime cuántas reseñas has analizado y su valoración media.
> 2. Agrupa los temas por frecuencia: cuántas reseñas mencionan cada uno. Ordénalos de más a menos frecuentes.
> 3. Para las reseñas de una o dos estrellas, explica las quejas principales.
> 4. Propón un plan de mejora. Usa solo quejas que aparezcan en al menos dos reseñas, y para cada una, una acción concreta y medible.
>
> No deduzcas problemas que no aparezcan en el texto.

**Qué cambia**

- El modelo declara su base de análisis antes de sacar conclusiones.
- Un tema que aparece una sola vez no se convierte en un problema general.
- El plan es verificable porque cada acción responde a una queja concreta.

**Prueba:** pendiente, con 5 o 6 reseñas reales sin nombres de autor.

---

## 4. Planificar: semana de clases especiales

**Versión vaga**

> Planifica una semana de clases especiales para mi gimnasio.

**Versión mejorada**

> Actúa como coordinador de eventos de un gimnasio. Te paso los datos de la semana del [fecha inicio] al [fecha fin].
>
> **Clases especiales a programar:**
> - [nombre de la clase], [duración], aforo máximo [número], sala [sala]
> - [nombre de la clase], [duración], aforo máximo [número], sala [sala]
> - [nombre de la clase], [duración], aforo máximo [número], sala [sala]
>
> **Trainers disponibles** (día y franja en la que pueden):
> - [nombre]: [días y horas]
> - [nombre]: [días y horas]
>
> **Reglas:**
> - Ningún trainer puede tener dos clases a la misma hora.
> - Máximo dos clases especiales por día.
> - Deja al menos un día sin clases especiales.
> - Si una restricción no se puede cumplir, dilo y no la ignores.
>
> Devuélveme una tabla con: día, hora, clase, trainer, sala, aforo y una tarea de comunicación para publicar antes de cada sesión. Después, lista los conflictos o datos que falten. No inventes nombres, horarios ni salas que no te he dado.

**Qué cambia**

- El modelo tiene las clases, los trainers y sus disponibilidades, así que no inventa horarios.
- Las reglas son comprobables: un trainer con dos clases a la misma hora es un error visible.
- Pedir la lista de conflictos evita que un plan incompleto parezca completo.

**Prueba:** pendiente, con tres clases y dos trainers ficticios.

---

## 5. Revisar: oferta de coaching

**Versión vaga**

> Revisa esta oferta de coaching y dime qué le falta.
>
> [pega el texto]

**Versión mejorada**

> Actúa como responsable comercial de un gimnasio que vende servicios de coaching personalizado. Te paso una oferta que voy a enviar a un cliente potencial.
>
> **Contexto del cliente:** [objetivo del cliente]
> **Precio y servicio:** [precio, sesiones por semana, nutrición incluida o no]
>
> **Revisa el texto según estos criterios:**
> 1. ¿Describe el servicio con datos concretos (sesiones, duración, seguimiento)?
> 2. ¿Responde al objetivo del cliente que te he indicado?
> 3. ¿Hay promesas que no se pueden garantizar (resultados exactos, plazos)? Señálalas.
> 4. ¿Tiene una llamada a la acción clara?
>
> Devuélveme: una lista de problemas por criterio, citando la frase exacta del texto, y una versión corregida de máximo 150 palabras. No inventes precios, servicios ni resultados que no aparezcan en el texto o en los datos que te he dado.
>
> Oferta:
> [pega el texto]

**Qué cambia**

- El modelo sabe a quién va dirigida la oferta y puede comprobar si encaja.
- Pedir la frase exacta obliga a señalar el problema en el texto, no en abstracto.
- El criterio de promesas protege frente a resultados garantizados, un riesgo real en coaching.

**Prueba:** pendiente, con una oferta breve que tenga dos errores conocidos.

---

## Lo que aprendí

- Los datos y las reglas importan más que el rol. El rol fija el tono, pero no sustituye a la información.
- Un prompt concreto se puede comprobar. Si no puedo verificar la respuesta, el prompt aún no está terminado.
- Pedir al modelo que diga qué datos le faltan es tan útil como pedirle la respuesta.
