# Material de apoyo

## Curso de procesamiento de lenguaje natural
## Maestría en Tecnologías de la Información
## Universidad Nacional de Misiones

Las libretas del curso están pensadas como un recurso
didáctico para explicar algunos de los temas vistos en el curso,
y al mismo tiempo mostrar como se pueden hacer estas cosas en *python*,
haciendo uso de las librerías especializadas.

Es por esta razón que en las libretas no es necesario hacer nada, ya todo
viene listo para ejecutarse y funcionar (dado lo reducido del tiempo frente a grupo).

## Como cargar las libretas del curso con el comando `git`

La manera más fácil de acceder a las carpetas es *clonar* el proyecto
en *github* donde se encuentran. Para esto, recomiendo que se instale
un contenedor de docker diseñado exclusivamente para el curso. Las instrucciones
para instalar el contenedor se pueden encontrar [aqui](https://unam-pln.github.io/2016/08/24/docker.html).

Los pasos son los siguientes:

1. Si ya tienes instalado el contenedor, pero no estás dentro, entrar
   con

```sh
$ docker start -i curso-pln
```

2. Ir al punto de montaje para que las libretas (y lo que generas con
   ellas) lo puedas ver fuera de tu contenedor.

```sh
~# cd curso-pln
```

3. Clonar el [proyecto de github con las
libretas](https://github.com/unam-pln/libretas-curso) en tu
repositorio.

```sh ~/curso-pln# git clone
https://github.com/unam-pln/libretas-curso.git
```

Sin embargo, no fue posible cargar un modelo de semántica distribuida,
ya que el tamaño del archivo era muy grande para *github*. Por esto hay que
hacer los siguientes pasos adicionales.

4. Ir a las libretas y crear un directorio modelo

```sh
~/curso-pln# cd libretas-curso/
~/curso-pln/libretas-curso# mkdir modelos
~/curso-pln/libretas-curso# cd modelos
```

y ya en la carpeta de modelos descargar el archivo con `wget`.

```sh
~/curso-pln/libretas-curso/modelos# wget -O fasttext-sbwc.vec.gz http://dcc.uchile.cl/%7Ejperez/word-embeddings/fasttext-sbwc.3.6.e20.vec.gz
```

La descarga es de unos 840MB, por lo que tarda su tiempo. Si se va a instalar en multples máquinas, es mejor copiar el archivo en una memoria USB y copiarlo en esta carpeta en cada máquina.


Listo, ya puedes usarlas solamente hay que ejecutar en el contenedor

```sh
~/curso-pln/libretas-curso/modelos# cd
~/curso-pln# run_notebook
```

Recomiendo y pido a todos los participantes en el curso que abran y
realicen los ejercicios que se piden en las dos libretas
preliminares. Estas libretas no las veremos en el curso pero dan una
idea de como utilizar las libretas así como los módulos de python
`numpy`, `matplotlib` y `pandas`aunque sea de manera superficial. Las
libretas preliminares (y el orden en que recomiendo las desarrollen)
son:

1. Preliminar- numpy.ipynb
2. Preliminar- pandas.ipynb

Si quieres saber algo más sobre jupyter y como funciona,
[aquí](https://juliowaissman.github.io/jupyter-intro/) hay una pequeña
presentación de jupyter hecha en jupyter.
