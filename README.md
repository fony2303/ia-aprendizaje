# Prompts reutilizables para gestión de un gimnasio

Primera pieza del portfolio del curso de IA generativa. Son cinco prompts, uno por tipo de tarea (redactar, analizar, resumir, planificar y revisar). Para cada uno incluyo la versión vaga, la versión mejorada, qué cambia entre ambas y el resultado de la prueba.

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

- **Versión vaga:** el post no menciona los eventos de noviembre y añade afirmaciones sobre instalaciones y atención que no se le dieron. Usa tres emojis, seis hashtags y no termina con una pregunta.
- **Versión mejorada:** anuncia los tres eventos con fecha, hora y trainer, usa un emoji, termina con una pregunta y no añade datos inventados. Cumple las 80 palabras aproximadas.

---

## 2. Analizar: KPI de trabajadoras

**Versión vaga**

> Revisa los KPI de mis trabajadoras y dime qué pueden mejorar.

**Versión mejorada**

> Actúa como responsable de operaciones de un gimnasio. Te pego a continuación una tabla con los datos de ventas y KPI de mis trabajadoras, del [fecha inicio] al [fecha fin], con las columnas: fecha, trabajadora, servicio, número de ventas, importe y [otros KPI]. "Plan amigo" significa número de altas con un amigo.
>
> Antes de analizar, dime si falta alguna de las columnas indicadas.
>
> Haz lo siguiente:
> 1. Agrupa los datos por trabajadora y por servicio. Calcula totales y medias por trabajadora, y muestra el cálculo de cada media antes del resultado.
> 2. Compara a cada trabajadora con la media del equipo. Usa solo los datos de la tabla; si falta un dato, dilo y no lo estimes.
> 3. Para cada trabajadora, escribe dos listas: qué ha hecho bien y qué focos mejorar. Cada punto debe citar una cifra concreta.
>
> Formato: una tabla resumen y después una sección por trabajadora. Máximo 300 palabras por trabajadora.

**Qué cambia**

- El modelo conoce las columnas y el periodo, así que sabe qué calcular.
- Avisa de los datos que faltan antes de empezar, en lugar de depender de que lo haga por iniciativa propia.
- Muestra el cálculo de las medias, así puedes comprobarlas.
- Cada conclusión tiene una cifra, lo que facilita verificar el análisis.

**Prueba** (con la tabla ficticia de Liss, Bea y Nei, del 9 al 15 de noviembre)

- **Versión vaga:** calcula bien los totales y las medias por trabajadora. Se equivoca en la media de NPS de Nei (8,2 en vez de 8,06). No avisa de que falta la columna de servicio.
- **Versión mejorada (versión anterior al cambio):** calcula bien los totales. Tiene el mismo fallo en la media de Nei. Avisa de que no hay columna de servicio y no inventa el NPS del domingo de Bea.
- **Pendiente:** repetir con el prompt ya actualizado para comprobar si el cálculo de medias mejora.

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
> No deduzcas problemas que no aparezcan en el texto. No inventes objetivos ni metas que no te he dado.

**Qué cambia**

- El modelo declara su base de análisis antes de sacar conclusiones.
- Un tema que aparece una sola vez no se convierte en un problema general.
- El plan es verificable porque cada acción responde a una queja concreta.
- No inventa objetivos numéricos que no aparezcan en los datos.

**Prueba** (con 8 reseñas ficticias, del 2 al 8 de noviembre)

- **Versión vaga:** agrupa las quejas en tres temas y da la media (3,0), que es correcta. Dice que dos de las tres reseñas sobre colas tienen 1 o 2 estrellas, cuando son las tres. No cuenta las frecuencias de forma explícita y no propone plan.
- **Versión mejorada:** las cifras son correctas (8 reseñas, media 3,0, cuatro reseñas de 1 o 2 estrellas con media 1,75). Cuenta las frecuencias en una tabla con los números de reseña. Deja fuera la queja aislada sobre la música, como pedía el prompt. Tiene dos fallos menores: habla de "la cliente" sin que se diga, y propone un objetivo de "no supere 5 minutos" que no sale de los datos. Por eso se añadió la última frase del prompt.

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

**Prueba** (con tres clases y tres trainers ficticios, semana del 16 al 22 de noviembre)

- **Versión vaga:** inventó clases (Pilates con aro, Bodycombat, un Maratón de Ritmo), un trainer que no existe en los datos (José) y horarios fuera de las franjas disponibles. Ignoró salas y aforos y añadió secciones que no pidió.
- **Versión mejorada:** usó solo las clases y los trainers dados, con su sala y aforo. Respetó las franjas, no hubo solapamientos y quedaron libres de jueves a domingo. Listó los huecos que no podía resolver sin preguntar: horas de inicio, reparto de días, frecuencia y horario de apertura.

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
> 5. ¿Incluye datos de confianza: titulación de quien atiende al cliente, condiciones de cancelación y un canal de contacto concreto? Señala los que falten.
>
> Devuélveme: una lista de problemas por criterio, citando la frase exacta del texto, y una versión corregida de máximo 150 palabras. No inventes precios, servicios ni resultados que no aparezcan en el texto o en los datos que te he dado. Si falta un dato para evaluar un criterio, dilo y no lo supongas.
>
> Oferta:
> [pega el texto]

**Qué cambia**

- El modelo sabe a quién va dirigida la oferta y puede comprobar si encaja.
- Pedir la frase exacta obliga a señalar el problema en el texto, no en abstracto.
- El criterio de promesas protege frente a resultados garantizados, un riesgo real en coaching.
- El criterio 5 evita que se pase por alto la falta de datos de confianza, que la versión vaga sí detectó.

**Prueba** (con una oferta ficticia que promete "8 kilos en 6 semanas" y no indica precio)

- **Versión vaga:** detectó la promesa de resultado garantizado y explicó el riesgo. Revisó más huecos que la versión mejorada, como titulación, políticas de cancelación y canal de contacto. Añadió consideraciones legales sin verificarlas, que hay que comprobar antes de citarlas.
- **Versión mejorada:** pidió los datos que faltaban antes de empezar. Evaluó los criterios que podía y citó frases exactas. No revisó titulación, políticas ni canal de contacto, porque el prompt no lo pedía. Por eso se añadió el criterio 5.
- **Pendiente:** repetir con el criterio 5 para comprobar que ahora sí detecta esos datos.

---

## Lo que aprendí

- Los datos y las reglas importan más que el rol. El rol fija el tono, pero no sustituye a la información.
- Un prompt concreto se puede comprobar. Si no puedo verificar la respuesta, el prompt aún no está terminado.
- Pedir al modelo que diga qué datos le faltan es tan útil como pedirle la respuesta.
- Una prueba vale más cuando anotas también los fallos de la versión mejorada, no solo sus aciertos.
