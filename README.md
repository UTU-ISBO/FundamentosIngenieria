### Cómo empujar Código Existente a un nuevo repositorio de GitHub

Para empujar código existente a un nuevo repositorio de GitHub, sigue estos pasos:

1. Copia el enlace HTTPS proporcionado al momento de crear el nuevo repositorio. Por ejemplo, [Repositorio Vacío(https://github.com/NombredeTuUsuario/Nombre_de_tu_repositor).

2. Ejecuta `git init` en la terminal. Esto inicializará la carpeta/repositorio que tienes en tu computadora local.

3. Ejecuta `git add .` en la terminal. Esto hará un seguimiento de los cambios realizados en la carpeta de tu sistema desde el último commit. Como esta es la primera vez que haces commit a los contenidos de la carpeta, se añadirán todos.

4. Ejecuta `git commit -m "inserta Mensaje aquí"`. Esto preparará los cambios añadidos/rastreados en la carpeta de tu sistema para empujar a GitHub. Puedes reemplazar "inserta el Mensaje aquí" con cualquier mensaje de confirmación relevante de tu elección.

5. Ejecuta `git remote add origin https://github.com/username/repository.git` en la terminal. Aquí, "username" y "repository" serán reemplazados por los valores proporcionados en el enlace copiado. Esto conectará la carpeta existente en tu sistema local al repositorio de GitHub recién creado.

6. Ejecuta `git remote -v`. Esto hace algo de magia usando `git pull` y `git push` para garantizar que el contenido de tu nuevo repositorio de GitHub y la carpeta en tu sistema local sean los mismos.

7. Finalmente, ejecuta `git push origin master` para empujar tus archivos a GitHub. Ten en cuenta que la última palabra en el comando "master", no es una entrada fija cuando se ejecuta `git push`, puede ser reemplazada por cualquier "nombre_de_rama" relevante.

¡Eso es todo! Sinceramente, creo que cualquiera puede aprender a programar. Pasé el año pasado dando clases particulares a estudiantes de pregrado en Nigeria sobre Desarrollo de Software.

¡Empieza hoy a programar! 🚀
