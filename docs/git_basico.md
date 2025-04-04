---
layout: default
title: Git Básico
nav_order: 5
---

# Comandos Básicos de Git

Esta guía contiene los comandos más comunes y útiles de Git para el control de versiones.

<iframe width="560" height="315" src="https://www.youtube.com/watch?v=2mxh3tgx71c" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Configuración Inicial

```bash
# Configurar nombre de usuario
git config --global user.name "Tu Nombre"

# Configurar email
git config --global user.email "tu@email.com"
```

## Comandos Esenciales

### Iniciar un Repositorio

```bash
# Crear un nuevo repositorio
git init

# Clonar un repositorio existente
git clone <url-del-repositorio>
```

### Manejo de Cambios

```bash
# Ver estado de archivos
git status

# Agregar archivos al área de preparación
git add <archivo>
git add .  # Agregar todos los archivos

# Crear un commit
git commit -m "Mensaje descriptivo del cambio"

# Ver historial de commits
git log
```

### Ramas (Branches)

```bash
# Crear una nueva rama
git branch <nombre-rama>

# Cambiar a una rama
git checkout <nombre-rama>

# Crear y cambiar a una nueva rama
git checkout -b <nombre-rama>

# Ver lista de ramas
git branch
```

### Sincronización con Repositorio Remoto

```bash
# Subir cambios al repositorio remoto
git push origin <nombre-rama>

# Obtener cambios del repositorio remoto
git pull origin <nombre-rama>

# Agregar un repositorio remoto
git remote add origin <url-repositorio>
```

## Ejemplos Prácticos

### Flujo Básico de Trabajo

```bash
# 1. Revisar estado actual
git status

# 2. Agregar cambios
git add index.html

# 3. Crear commit
git commit -m "Actualización del archivo index.html"

# 4. Subir cambios
git push origin main
```

### Trabajar con Ramas

```bash
# 1. Crear rama para nueva característica
git checkout -b feature/nueva-funcionalidad

# 2. Realizar cambios y commits
git add .
git commit -m "Agregada nueva funcionalidad"

# 3. Volver a la rama principal
git checkout main

# 4. Fusionar cambios
git merge feature/nueva-funcionalidad
```

## Consejos Útiles

- Siempre verifica en qué rama estás trabajando antes de hacer cambios
- Haz commits frecuentes y con mensajes descriptivos
- Mantén tu repositorio local actualizado con `git pull` antes de empezar a trabajar
- Usa `.gitignore` para excluir archivos que no deben versionarse

## Solución de Problemas Comunes

```bash
# Deshacer último commit (manteniendo cambios)
git reset --soft HEAD~1

# Descartar cambios en archivos no commiteados
git checkout -- <archivo>

# Ver diferencias entre archivos
git diff
```