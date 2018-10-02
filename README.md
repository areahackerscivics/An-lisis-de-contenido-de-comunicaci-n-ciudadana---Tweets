# Análisis de contenido de comunicación ciudadana - Tweets


## Descripción

Los diferentes ayuntamientos mantienen abiertos canales de comunicación con la ciudadanía.
Entendemos que la información generada a través de esta interacción puede ser muy útil para
conocer lo que les interesa a los ciudadanos.
Por eso es necesario identificar los canales de comunicación más relevantes incluidos redes
sociales y seleccionar aquellos que aportarán mayor valor (periodicidad, consistencia,
pertinencia y confiabilidad) para convertirlos en fuente de datos.
El procesamiento de la información se hará a través de técnicas de Búsqueda y Recuperación
de información y algoritmos de aprendizaje automático para realizar la clasificación de la
información basado en la taxonomía de sectores primarios recogida en la Guía de aplicación de
la Norma Técnica de Interoperabilidad relativa a la Reutilización de recursos de información
(página 42 y 43).

Una vez generado el sistema de clasificación se deberá crear un informe comparativo entre los
temas que habla la gente y los datos publicados por el ayuntamiento. Con esto se puede ver si
lo que están solicitando los ciudadanos es lo que se está publicando y promover la apertura de
los datos desde la demanda de la ciudadanía.


## Funcionamiento del proyecto

Este proyecto consta de dos módulos:
- **Módulo 1. Clasificación**:
  - [**Descarga**](https://github.com/areahackerscivics/AC_M1_DescargaTweet). Se encarga de la búsqueda y descarga de tweets.
  - [**Clasificación**](https://github.com/areahackerscivics/AC_M1_Clasificacion). Gestiona la
clasificación de tweets y sus análisis.
 -   [**Catálogo**](https://github.com/areahackerscivics/AC_M1_Catalogo). Gestiona la búsqueda y descarga del catálogo de datos abiertos publicado por el ayuntamiento de valencia.

- **Módulo 2. Reportes**:
  - [**API**](https://github.com/areahackerscivics/AC_M2_ReporteAPI). API REST para devolver la información de los análisis.
  - [**Visualización reportes**](https://github.com/areahackerscivics/AC_M2_Reportes).Código de la web que muestra la comparación de lo que hablan las personas a lo que ofrece el Ajuntament de València.
  - [**Resultado**]( https://marymatt.github.io/).




Si deseas utilizar el proyecto, primero de todo necesitarás una base de datos MongoDB y un servidor. Utilizando el
módulo _DescargaTweet_ realizarás la descarga de tweets, se recomienda que ejecutes este módulo en el servidor.
Una vez tengas un buen _corpus_ de tweets, puedes entrar al panel de control con el módulo _GeneradorInformesTwitter_.

Este punto es crítico y se recomienda disponer de unos pocos conocimientos en Aprendizaje Automático (_Machine Learning_) y más concretamente, en técnicas para
tratamiento de textos (Bag of Words, Steamming, Regex...). Necesitarás disponer de
un _clasificador_, por lo que, entrando en _Administrar/Listar Clasificadores_ puedes
gestionar un _clasificador_. La creación (entrenamiento) del _clasificador_ puede
tardar un poco, ten paciencia. Cuando ya tienes el clasificador, en el apartado
_Administrar/Clasificar_ puedes ver un listado por fecha, el número de tweets que
dispone. Marcnado en la casilla, seleccionas las fechas a clasificar.

Con tweets clasificados en la base de datos, ya puedes arrancar el servicio REST (módulo _ReporteAPI_). Con este servicio en marcha, puedes ver los resultados a través
del módulo _WebInformes_ o tu o cualquier otra persona, puede hacerse una aplicación propia para consultar a este servicio.

## Equipo
- Autores principales:  
  - **<a href="https://www.linkedin.com/in/marylin-mattos-a0a59b22/" target="_blank"> Marylin Mattos Barros</a>**, estudiante de Máster Oficial Universitario en Gestión de la Información


- Director del proyecto:
  - [Diego Álvarez](https://about.me/diegoalsan) | @diegoalsan


## Contexto del proyecto

El trabajo que contiene este repositorio se ha desarrollado en el [**Àrea Hackers cívics**](http://civichackers.cc). Un espacio de trabajo colaborativo formado por [hackers cívics](http://civichackers.webs.upv.es/conocenos/que-es-una-hacker-civicoa/) que buscamos y creamos soluciones a problemas que impiden que los ciudadanos y ciudadanas podamos influir en los asuntos que nos afectan y, así, construir una sociedad más justa. En definitiva, abordamos aquellos retos que limitan, dificultan o impiden nuestro [**empoderamiento**](http://civichackers.webs.upv.es/conocenos/una-aproximacion-al-concepto-de-empoderamiento/).

El [**Àrea Hackers cívics**](http://civichackers.cc) ha sido impulsada por la [**Cátedra Govern Obert**](http://www.upv.es/contenidos/CATGO/info/). Una iniciativa surgida de la colaboración entre la Concejalía de Transparencia, Gobierno Abierto y Cooperación del Ayuntamiento de València y la [Universitat Politècnica de València](http://www.upv.es).

![ÀHC](http://civichackers.webs.upv.es/wp-content/uploads/2017/02/Logo_CGO_web.png) ![ÀHC](http://civichackers.webs.upv.es/wp-content/uploads/2017/02/logo_AHC_web.png)



## Términos de uso

El contenido de este repositorio está sujeto a la licencia [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html). ![](https://www.gnu.org/graphics/gplv3-127x51.png)
