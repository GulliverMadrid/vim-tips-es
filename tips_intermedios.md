# Vim - Tips Intermedios

En una búsqueda, se usa `n` para ir al siguiente resultado, y `N` para cambiar la dirección de búsqueda.

Para recargar los ajustes en una ventana ya abierta: `:source $MYVIMRC`.

Para moverse por líneas de pantalla, se antepone `g`: `gj`,`gk`, `g$`, `g0`,
`g^`.

Para cancelar una secuencia de comandos, se usa `ctr-C`.

Se pueden definir comandos personalizados con `:command`. Ejemplo:
```vim
:command Holamundo echom "Hola mundo"
```

### Colores
Para ver los colores activos, se usa `:highlight`.

### Autocomandos
Conviene crearlos dentro de un grupo e iniciarlo con `autocmd!` para que no se definan varias veces en caso de recargar `vimrc`.

### Navegar por los comandos
Para navegar por el historial de comandos, se usa `:` y desde ahí, `ctr-P` para ir hacia atrás, y `ctr-N` para ir hacia adelante.

### Folding
Para alternar el plegado, se usa `za`. Para crear un plegado nuevo, `zf{motion}`. Por ejemplo, `zf4j` para plegar hasta 4 líneas más abajo.
Más info: https://vim.fandom.com/wiki/Folding

### Iniciar sin settings
Para iniciar vim en modo `nocompatible`, pero sin usar vimrc, se usa `vim -N -u NONE`. Esto puede ser útil para chequear el comportamiento por defecto de Vim, sin mappings, plugins, etc.

### Añadir el contenido de un registro a la línea de comandos
Desde la línea de comandos de Vim, pulsar ctr-R y el simbolo del registro que se quiera añadir.

## Plugins

### Cómo instalar plugins en vim (usando vim-plug)
- Instalar el gestor de plugins desde `https://github.com/junegunn/vim-plug`.
- Después de instalarlo, puede que sea necesario cambiar la ubicación del directorio de configuración de Vim, usar un symlink para que sea compatible con la Bash, etc. Esto depende del sistema operativo y del terminal que vayamos a usar.
- En nuestro vimrc, pondremos la siguiente línea: 
```vim
call plug#begin(<ruta-del-directorio-de-plugins>)
```
La ruta será aquella en la que queramos que se almacenen los plugins, como por ejemplo `'~/.vim/plugged'`. A continuación, los plugins que queramos utilizar, con la sintaxis
```vim
Plug 'nombre_creador/nombre_plugin'
```
Y finalmente: 
```vim
call plug#end()
```
Además, cada vez que añadamos plugins a la lista, habrá que ejecutar manualmente `:PlugInstall`.

