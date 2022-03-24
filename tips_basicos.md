# Vim Hints

## Moverse por palabras

`b` inicio palabra  
`e` final palabra  
`w` siguiente palabra  
`ge` anterior fin de palabra  

## Moverse en la línea

`$` final de la línea  
`0` / `^^` inicio de la línea  
`f{c}` ir hacia adelante hasta el carácter {c}  
`F{c}` ir hacia atrás hasta el carácter {c}  

## Saltar

`G` saltar al final del documento  
`:20` / `20G` saltar a la línea 20  
`<C-F>` Bajar una página (f de 'forward')
`<C-B>` Subir una página (b de 'back')

## Insertar

`i` insertar antes del cursor  
`a` añadir después del cursor  
`A` añadir al final de la línea  
`o` insertar en la línea inferior  
`O` insertar en la línea superior  

## Borrar

`x` borrar carácter  
`dw` borrar palabra  
`dd` borrar linea  
`d$` borrar hasta final linea  

## Reemplazar

`r` reemplazar un carácter  
`R` reemplazar varios caracteres  
`cw` cambiar palabra (desde el cursor)  
`c$` cambiar hasta final línea  
`s` x + i (borra el caracter y pasa al modo insert)  

## Deshacer / rehacer

`u` deshacer  
`U` deshacer línea  
`<C-R>` rehacer  

## Pegar

`p` pegar después  
`P` pegar antes  

## Modo visual

`v` activar modo visual  
`d` / `x` borrar selección  
`y` copiar selección  
`s` reemplazar selección  

## Buscar

`/` busca una cadena hacia abajo  
`?` busca una cadena hacia arriba  
`n` busca la siguiente coincidencia  
`%` busca el otro paréntesis  

## Sustituir cadenas...

`:s/vieja/nueva` una vez  
`:s/vieja/nueva/g` todas las ocurrencias hasta el final de línea  
`:40,50s/vieja/nueva/g` todas las ocurrencias entre la línea 40 y la 50  
`:%s/vieja/nueva` una ocurrencia por línea en todo el documento  
`:%s/vieja/nueva/gc` todas las ocurrencias en todo el documento (pidiendo confirmación para cada caso)
`:%s/\<vieja\>/nueva/g` todas las ocurrencias en todo el documento (palabras completas)

## Ajustes

`:set <option>` fija la opción correspondiente (con ! al final la alterna)

## Atajos en el modo visual

En el modo visual, con `u` se pasa a minúsculas y con `U` se pasa a mayúsculas.

## Atajos con ctr en el modo insertar

#### Borrar a la izquierda:

  `<C-H>` un caracter
  `<C-W>` una palabra  
  `<C-U>` todos los caracteres nuevos / toda la línea

#### Otros:

`<C-T>` / `<C-D>` aumentar / reducir indentación de la línea  
`<C-N>` / `<C-P>` siguiente / anterior coincidencia de autocompletado  
`<C-R{x}>` insertar el contenido del registro {x}  
`<C-O{x}>` entrar temporalmente en el modo normal para ejecutar el comando {x}  
`<C-A>` insertar el texto previamente insertado  
`<C-Y>` / `<C-E>` Insertar el carácter que se encuentra justo encima / abajo del cursor

### Folders

`zM` pliega todos los folders  
`zR` despliega todos los folders  
`za` alterna el folder actual  
