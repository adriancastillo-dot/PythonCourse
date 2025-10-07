#PracticasPA

Nombre:  Adrián Castillo Acosta

Titulación: GIT

Preguntas:

Ejercicio 1: ¿Por qué se utiliza la lista por comprensión [p.lower() for p in palabras_remplazo] en lugar de un bucle tradicional para convertir las palabras a minúsculas?

    Respuesta: Porque una lista por comprensión permite realizar la misma operación en una sola línea, generando una nueva lista sin necesidad de usar append() dentro de un for. Además, suele ser más eficiente y más legible cuando la operación es sencilla.

    Observación personal: Antes usaba bucles for normales, pero al ver esta forma me di cuenta de que el código queda mucho más limpio y rápido de entender.

    Mejora: La IA me sugirió que, si no necesito una lista nueva, use un generador ((p.lower() for p in ...)) para ahorrar memoria.

Ejercicio 2: ¿Por qué en la función is_prime() se recorre hasta int(n**0.5) + 1 y no hasta n?

    Respuesta: Porque basta con comprobar divisores hasta la raíz cuadrada de n. Si un número no tiene divisores menores o iguales a su raíz cuadrada, no los tendrá mayores. Esto mejora mucho la eficiencia.

    Observación personal: Me sorprendió que un cambio tan pequeño acelerara tanto la ejecución, sobre todo al generar listas largas de primos.

    Mejora: La IA me recomendó usar la criba de Eratóstenes si quiero calcular muchos primos rápidamente.

Ejercicio 3: ¿Qué ventaja tiene usar str(p) == str(p)[::-1] para detectar palíndromos?

    Respuesta: Esta expresión convierte el número en texto y lo compara con su versión invertida. Si son iguales, el número se lee igual al derecho y al revés, por lo que es palíndromo.

    Observación personal: Me pareció una manera muy elegante y compacta. Antes lo hacía con bucles, pero esta forma es mucho más eficiente.

    Mejora: La IA me recomendó convertir el número solo una vez a cadena y guardarlo antes de compararlo, para evitar trabajo repetido.

Ejercicio 4: ¿Por qué en la función task_manager() se define otra función dentro (modify_task())?

    Respuesta: Para demostrar el uso de funciones anidadas y variables no locales. Gracias a nonlocal, la función interna puede modificar variables de la función que la contiene sin necesidad de declararlas globales.

    Observación personal: No conocía esta forma de estructurar código. Me parece útil cuando una función solo tiene sentido dentro de otra.

    Mejora: La IA me sugirió usar un contador interno (cambios_realizados) para practicar el uso de nonlocal de una forma más completa.

Ejercicio 5: ¿Por qué en subcad_cont() se usa sum(1 for i in cadenas if subcadena in i.lower())?

    Respuesta: Porque evalúa la condición subcadena in i.lower() para cada cadena y suma 1 cada vez que es verdadera. Es más legible y compacto que un for con contador.

    Observación personal: No sabía que True se podía sumar como si fuera 1, me pareció curioso y práctico.

    Mejora: La IA me explicó que si solo quiero saber si existe alguna coincidencia puedo usar any() para hacerlo aún más eficiente.

Ejercicio 6: ¿Por qué se usa re.sub() en lugar de modificar el texto línea por línea para anonimizar el informe?

    Respuesta: Porque re.sub() permite buscar y reemplazar texto basándose en patrones, no solo en coincidencias exactas. Esto hace que funcione incluso si hay variaciones en espacios o formato.

    Observación personal: Al principio me costó mucho entender cómo funcionan las expresiones regulares y las sustituciones, pero cuando lo entendí vi que con pocas líneas podía reemplazar nombres, fechas y médicos de manera automática.

    Mejora: La IA me enseñó a usar grupos con nombre (?P<d>, ?P<m>, ?P<y>) dentro de los patrones para poder acceder fácilmente al día, mes y año al calcular la edad.

Ejercicio 6: ¿Por qué es necesario calcular la edad a partir de la fecha de nacimiento y una fecha de referencia en el informe médico?

    Respuesta: Porque el informe puede contener varias fechas (por ejemplo, fecha de nacimiento y fecha del informe), y para que la edad sea coherente, hay que usar la fecha más reciente como referencia. Si no se hiciera así, la edad calculada podría ser incorrecta si el informe no es del mismo año.

    Observación personal: Este fue el apartado que más me costó. Me confundía el manejo de fechas con datetime y la forma de restar años correctamente. Después de pedir ayuda a la IA entendí que hay que comparar mes y día para saber si el cumpleaños ya pasó o no.

    Mejora: La IA me recomendó crear una función calcular_edad(nac, ref) que reste los años y ajuste según la fecha actual, lo que dejó el código mucho más limpio y reutilizable.

Las preguntas y las consultas sobre el código se han realizado mediante el modelo de LLM ChatGPT 5