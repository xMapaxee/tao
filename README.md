# Tao_Te_King


## Finalidad de este repositorio

Debido al la gran cantidad de capítulos y a la pequeña longitud de sus líneas, es un texto que se presta bien para realizar prácticas de control de versiones. Por tanto será usado para realizar actividades de este tipo y probar los comandos disponibles en GIT. 


## Acerca de  ...

**El libro del Camino y la Virtud**

El Dào Dé Jīng (Chino: 道德經, Tao Te Ching, también llamado Tao Te King), es un texto clásico chino cuya autoría se atribuye a Laozi (Lao Tse, "Viejo Maestro").

Es uno de los fundamentos del **taoísmo** filosófico y tuvo una fuerte influencia sobre otras escuelas, como el legalismo y el neoconfucianismo. Tiene un papel importante en la religión china, relacionado no sólo con el taoísmo religioso, sino también con el budismo, que cuando se introdujo por primera vez en China fue interpretado usando en gran medida palabras y conceptos taoístas.

En sus 81 capítulos, a través de diversos aforismos de estética poética, el autor define la sabiduría práctica, da consejo a los gobernantes, e incluso parece adentrarse en los misterios alquímicos que confieren la inmortalidad.

Más información acerca del libro:
- https://es.wikipedia.org/wiki/D%C3%A0od%C3%A9_j%C4%ABng

## Procesado de texto

El texto ha sido obtenido desde https://es.wikisource.org/wiki/Tao_Te_King y copiado a [Tao_Te_King.txt](texto/Tao_Te_King.txt). Está en formato Unicode UTF-8. 

Para dar formato a algunos saltos de página y tabulaciones y crear los capítulos se han usado los siguientes comandos de la shell:

```bash
sed s/"Capítulo"/"\n\nCapítulo"/g Tao_Te_King.txt | sed s/"\t"/"\n\n"/g - | csplit -f Cap -b %02d.txt  -  '/^Capítulo*/' '{*}'  && rm Cap00.txt
```

