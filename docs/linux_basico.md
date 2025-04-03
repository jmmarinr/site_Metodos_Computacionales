---
layout: default
title: Linux Básico
nav_order: 6
---

# Comandos Básicos de Linux

Esta guía contiene los comandos más comunes y útiles de la terminal de Linux.

## Navegación y Gestión de Archivos

```bash
# Mostrar directorio actual
pwd

# Listar contenido del directorio
ls
ls -l    # Formato largo
ls -a    # Mostrar archivos ocultos
ls -lh   # Formato largo con tamaños legibles

# Cambiar de directorio
cd /ruta/del/directorio
cd ..    # Subir un nivel
cd ~     # Ir al directorio home
cd -     # Volver al directorio anterior

# Crear directorios
mkdir nombre_directorio
mkdir -p dir1/dir2/dir3    # Crear estructura de directorios

# Copiar archivos/directorios
cp archivo1 archivo2
cp -r directorio1 directorio2    # Copiar directorios

# Mover/renombrar archivos
mv archivo1 archivo2
mv archivo directorio/

# Eliminar archivos/directorios
rm archivo
rm -r directorio    # Eliminar directorio y contenido
rm -f archivo      # Forzar eliminación
```

## Visualización y Edición de Archivos

```bash
# Ver contenido de archivos
cat archivo.txt
less archivo.txt    # Ver por páginas
head archivo.txt    # Primeras 10 líneas
tail archivo.txt    # Últimas 10 líneas
tail -f archivo.log # Seguir archivo en tiempo real

# Editores de texto
nano archivo.txt    # Editor simple
vim archivo.txt     # Editor avanzado
```

## Sistema y Procesos

```bash
# Información del sistema
uname -a           # Información del kernel
df -h             # Espacio en disco
free -h           # Memoria disponible
top               # Monitor de procesos
htop              # Monitor de procesos (mejorado)

# Gestión de procesos
ps aux            # Ver procesos en ejecución
kill PID          # Terminar proceso por ID
killall nombre    # Terminar proceso por nombre
```

## Permisos y Usuarios

```bash
# Ver permisos
ls -l

# Cambiar permisos
chmod 755 archivo    # Modo numérico
chmod u+x archivo    # Modo simbólico

# Cambiar propietario
chown usuario:grupo archivo

# Usuario actual
whoami

# Cambiar a superusuario
sudo comando
su -               # Cambiar a root
```

## Búsqueda y Filtrado

```bash
# Buscar archivos
find /ruta -name "nombre"
locate archivo

# Buscar en contenido
grep "texto" archivo
grep -r "texto" directorio/

# Filtrar salida
comando | grep "filtro"
```

## Red y Conectividad

```bash
# Información de red
ifconfig    # Interfaces de red
ip addr     # Alternativa moderna
ping host   # Probar conectividad
netstat -an # Conexiones activas

# Transferencia de archivos
wget url    # Descargar archivo
curl url    # Hacer peticiones HTTP
scp archivo usuario@host:/ruta    # Copiar por SSH
```

## Compresión de Archivos

```bash
# Comprimir
tar -czf archivo.tar.gz directorio/
zip -r archivo.zip directorio/

# Descomprimir
tar -xzf archivo.tar.gz
unzip archivo.zip
```

## Consejos Útiles

- Usa la tecla Tab para autocompletar comandos y rutas
- Usa las flechas arriba/abajo para navegar el historial de comandos
- `history` muestra el historial de comandos
- `man comando` muestra el manual del comando
- Ctrl+C cancela el comando actual
- Ctrl+L limpia la pantalla

## Redirección y Pipes

```bash
# Redirección
comando > archivo.txt      # Redirigir salida
comando >> archivo.txt     # Añadir al final
comando 2> error.log      # Redirigir errores

# Pipes (tuberías)
comando1 | comando2       # Conectar salida y entrada
```