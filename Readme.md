PEOYECTO-P1_01
Primer proyecto Individual

image

HENRY'S LABS
#Tematica El proyecto consistía en situarse en el rol de Data Scientist, a quien como miembro del equipo de una empresa, se nos solicita realizar un análisis sobre cuatro datasets proporcionados, conteniendo información relativa a los catálogos de series y películas de cuatro plataformas de streaming (Netflix, Hulu, Amazon Prime Video y Disney).

Como segunda parte del requerimiento, se solicitaba elaborar una API a efectos de disponibilizar los datos de manera online, los cuales debían poder visualizarse mediante consultas predefinidas.

Por último, se solicita documentar todo el proceso y el funcionamiento de la API.

Rol a Desarrollar
Empezaste a trabajar como Data Scientist en una start-up que provee servicios de agregación de plataformas de streaming. El mundo es bello y vas a crear tu primer modelo de ML que soluciona un problema de negocio: un sistema de recomendación que aún no ha sido puesto en marcha!

Vas a sus datos y te das cuenta que la madurez de los mismos es poca (ok, es nula 😭): Datos sin transformar, no hay procesos automatizados para la actualización de nuevas películas o series, entre otras cosas…. haciendo tu trabajo imposible 😩.

Debes empezar desde 0, haciendo un trabajo rápido de Data Engineer y tener un MVP (Minimum Viable Product) para la próxima semana! Tu cabeza va a explotar 🤯, pero al menos sabes cual es, conceptualmente, el camino que debes de seguir ❗. Así que te espantas los miedos y te pones manos a la obra 💪

Detalles del requerimiento

Procesaciento de datos:
Se solicitó efectuar las siguientes transformaciones sobres los datos provistos:

Generar campo id: Cada id se debía componer de la primera letra del nombre de la plataforma, seguido del show id ya presente en los datasets (ejemplo: para títulos de Amazon = as123)
Los valores nulos del campo rating debía reemplazarse por el string “G” (corresponde al maturity rating: “general for all audiences”
De haber fechas, debían tener el formato AAAA-mm-dd
Los campos de texto debían estar en minúsculas, sin excepciones
El campo duration debía convertirse en dos campos: duration_int y duration_type. El primero con formato integer y el segundo string, indicando la unidad de medición de duración; min (minutos) o season (temporadas).
Desarrollo API: Propones disponibilizar los datos de la empresa usando el framework FastAPI. Las consultas que propones son las siguientes:

Película con mayor duración con filtros opcionales de AÑO, PLATAFORMA Y TIPO DE DURACIÓN. (la función debe llamarse get_max_duration(year, platform, duration_type))

Cantidad de películas por plataforma con un puntaje mayor a XX en determinado año (la función debe llamarse get_score_count(platform, scored, year))

Cantidad de películas por plataforma con filtro de PLATAFORMA. (La función debe llamarse get_count_platform(platform))

Actor que más se repite según plataforma y año. (La función debe llamarse get_actor(platform, year))

Tecnologias empleadas:
Pandas
Numpy
FastAPI
DETA