https://gist.github.com/eviera/6df5ca2a8065bb821031b1b29c933270

# Notas Kotlin-Android

## Diseño

- En _font-family_ , _more fonts..._ se pueden usar fonts descargables
- Boton derecho sobre los objetos editados permite centrar automaticamente usando las constraints
- _match_constraints_ se expande en horizontal o vertical hasta donde puede. Hay que ponerle un 
aspect ratio correcto. Para portrait de telefonos, se puede usar 1:1 y para landscape 16:9
- _match_constraints_ a veces al querer que dos elementos sean iguales en tamaño, uno queda mucho mas grande
que el otro. Esto es porque el primero de ellos tiene alguna constraint de mas (por ejemplo hay que 
quitarle una de las constraints del costado). Ver proyecto **UdemyKotlinAndroidDevProfile**
- _match_constraints_ cuando se setean las match_constraints para un objeto, primero hay que setear 
ambas en el objeto (click sobre los 'tensores' del objeto), y **luego** poner el aspect ratio (1:1 o 16:9)
- Se pueden (deben) crear layouts con el mismo nombre, usando los qualifiers (en el dialogo de creación)
pasandole, por ejemplo, size=x-large, o orientation=landscape
- Se puede redondear una imagen en código:
```kotlin
        val bitmap = BitmapFactory.decodeResource(resources, R.drawable.devslopesprofilelogo)
        val rounded = RoundedBitmapDrawableFactory.create(resources, bitmap)
        rounded.cornerRadius = 15f
        //rounded.isCircular = true
        logo.setImageDrawable(rounded)
```
- Cadenas
  - Para encadenar (chain) varios elementos, seleccionarlos y con boton derecho crear una horizontal
o vertical chain
  - Los objetos encadenados se pueden 'correr' a izquierda o derecha usando el slider de bias (ej: `app:layout_constraintHorizontal_bias="0.8"`)
  - Los objetos encadenados tienen una cabeza (head), que es desde la cual se pueden poner constraints
que afectan a todos los objetos
  - Los objetos encadendos se pueden separar entre si, poniendoles un layout margin
  - Cuando los objetos estan encadenados aparece un icono de cadena en ellos. Al clickearlo se puede
  ciclar por los distintos modos de cadena
- Para que varios objetos queden alineados, seleccionarlos y con boton derecho elegir _Align vertical centers_. 









(ref: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)