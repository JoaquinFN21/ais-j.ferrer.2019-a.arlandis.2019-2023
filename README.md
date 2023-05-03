# AIS-Practica-3-2023

Autor(es): Adrian Arlandis Alonso y Joaquin Ferrer Nuñez

[Repositorio](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023)

[Aplicación Okteto](https://books-reviewer-joaquinfn21.cloud.okteto.net/)

## Desarrollo con (GitFlow/TBD)

Antes de seguir con los pasos hay que tener en cuenta unas cuantas consideraciones. La mayoria de los actions e imagenes que aparecen creadas son de pruebas realizadas forzosamente para comprobar que se creaban correctamente. Por ejemplo, las imagenes creadas por el Workflow3 son correctas las que se crean a partir del dia 03/05/2023. 

Una vez creadoas los workflows y funcionando estos, pasamos a crear la nueva funcionalidad utilizando (Gitflow o TBD):

1. Creacion de la rama develop a partir de la rama master.
2. Creacion de la rama feature/libros-descripcion a partir de la rama develop. Se ejecuto Workflow 1 ya que conto como un push hacia esa rama: [ActionPaso2](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4863324536)
3. Cambio realizado en la clase BookDetail para que la descripciones de mas de 950 caracteres finalicen en 3 puntos. Al ser un commit en la rama feature/libros-descripcion se ejecuta el Workflow1. [ActionPaso3](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4863333170)
4. Se realiza un pull request para mezclar la rama feature con la rama develop. Se ejecuta el Workflow1 al ser un pull-request sobre la rama develop: [ActionPaso4](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4863355523)
5. Al mezclar la rama cuenta como un push sobre la rama develop, por lo que tambien se ejecuta el Workflow2. [ActionPaso5](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4863371051)
6. Se crea una rama release/0.2.0 a partir de la rama develop. Al hacer esto cuenta como un push sobre la rama release, por lo que se ejecuta el Workflow4. [ActionPaso6](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4863379840)
7. Actualizamos el pom de release quitando SNAPSHOT de la version. Al hacer un commit se ejecuta el Workflow4. [ActionPaso7](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4863417913)
8. Actualizamos tambien la version que aparece en el archivo docker-compose, por lo que tambien se ejecuta el Workflow4. [ActionPaso8](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4863433320)
9. Actualizamos el pom de la rama develop, preparando la siguiente version(0.3.0-SNAPSHOT). Se ejecuta el Workflow2 al ser un commit sobre esta rama. [ActionPaso9](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4863446330)
10. Realizamos un pull-request para mezclar la rama release/0.2.0 sobre la rama master. Al hacer esto, se ejecuta el Workflow5, encargado de desplegar la aplicacon en Okteto. [ImagenDocker](https://hub.docker.com/layers/repo2001/ais-j.ferrer.2019-a.arlandis.2019-2023/0.2.0/images/sha256-02b32ba2c2a5e44b12c07c8c647838dd3c86e249e5cb722e5202d4d857839a99?context=explore) [ActionPaso10](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4863467265)
11. Si se entra en el enlace de aplicacion Okteto se puede ver como la funcionalidad ha sido añadida correctamente.
Extra. Respecto al Workflow3 esta programado para que se ejecute todos los dias por la noche. [ImagenWorkflow3](https://hub.docker.com/layers/repo2001/items/dev-20230503.005008/images/sha256-02b32ba2c2a5e44b12c07c8c647838dd3c86e249e5cb722e5202d4d857839a99?context=repo) [ActionPasoExtra](https://github.com/JoaquinFN21/ais-j.ferrer.2019-a.arlandis.2019-2023/actions/runs/4867174632)
