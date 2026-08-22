# Buenas Prácticas de Versionado
Para mantener el repositorio limpio y entendible, tratemos de seguir estas reglas:

### 1. Manejo de las Ramas
* **a.** Cada uno va a clonar el repo a su PC.
* **b.** Desde `main`, cada uno se va a crear una rama local basada en `main`.
* **c.** Los cambios se van a hacer sobre su rama local.
* **d.** Una vez probados los cambios en su rama local y que funcione correctamente, deben pushearlos.
  * **d.1. Cómo pushear correctamente:**
    * **d.1.1.** Primero, antes de pushear, hay que asegurarnos de no generar conflictos con código que un compañero haya pusheado previamente.
    * **d.1.2.** Antes de pushear nuestros cambios, vamos a tirar un pull origin, que nos va a traer las últimas actualizaciones que se hayan hecho en la rama `main`.
    * **d.1.3.** Luego de tirar el pull y corroborar que no existan conflictos de código, recién ahora podemos pushear.
* **e.** De esta manera siempre mantenemos actualizadas nuestras ramas.
* **f.** Tampoco va a ser una locura de conflictos, pero de paso está bueno aplicar estas buenas prácticas.

### 2. Mensajes de Commit Claros
Evitemos los mensajes genéricos. Usemos un formato que explique qué se hizo:

* `[ADD]` para archivos nuevos o funciones nuevas.
* `[FIX]` para cuando arreglamos un error.
* `[DEL]` para cuando queremos borrar algo (muy difícil que pase pero no hay que descartarlo, siempre van a ser fixes o adds).
* **Ejemplos:** 
  `git commit -m "[FIX] Corregido error de punteros en la función de búsqueda"`.
  `git commit -m "[ADD] nueva funcionalidad (breve desc)"`.


### 3. Sincronización (Pull antes de Push)
Antes de empezar a programar y antes de subir tus cambios:

Hacé un Pull para bajarte lo que hicieron los demás:

* `git pull origin main`  Trae los últimos cambios que se pushearon en main
* Resolvé los conflictos (si los hay) localmente.

Ahí recién hacé el Push de tus cambios:

* `git push origin main ` Luego de traer los últimos cambios a mi rama y validar que no hay conflictos, pusheo mis cambios a main
  
### 4. Commits Pequeños
Es mejor hacer 5 commits que expliquen pasos distintos, que un solo commit gigante con todo el TP. Esto nos permite volver atrás fácilmente si algo deja de funcionar.

### 5. No "Romper" la Rama Principal
Tratemos de que lo que subamos al main sea código que al menos compile. Si estás probando algo que todavía no funciona, avisá por el grupo de WhatsApp antes de subirlo.
