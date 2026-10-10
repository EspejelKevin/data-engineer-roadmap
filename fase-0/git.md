# Investigación: Comandos Esenciales de Git 🚀

Esta investigación documenta el propósito, funcionamiento y ejemplos prácticos de los cuatro pilares fundamentales del control de versiones con Git: `add`, `commit`, `branch` y `merge`.

---

## 🛠️ Comandos Principales

### 1. Git Add
* **¿Qué es?** Mueve los cambios de los archivos desde el directorio de trabajo hacia el área de preparación (*staging area*). Define qué modificaciones se incluirán en la próxima confirmación.
* **Ejemplo:**
  ```bash
  # Añadir un archivo específico
  git add index.html

  # Añadir todos los archivos modificados
  git add .
  ```

### 2. Git Commit
* **¿Qué es?** Guarda de forma permanente en el historial del repositorio los cambios previamente preparados, creando una "fotografía" (*snapshot*) del proyecto con un mensaje descriptivo.
* **Ejemplo:**
  ```bash
  git commit -m "Añade formulario de contacto en la página principal"
  ```

### 3. Git Branch
* **¿Qué es?** Crea, lista o elimina ramas. Permite abrir líneas de desarrollo independientes para trabajar en nuevas funciones o correcciones sin alterar el código principal.
* **Ejemplo:**
  ```bash
  # Crear y cambiarse a una nueva rama
  git switch -c nueva-funcion
  ```

### 4. Git Merge
* **¿Qué es?** Une el historial y los cambios de una rama secundaria dentro de otra rama (generalmente la rama principal como `main` o `master`).
* **Ejemplo:**
  ```bash
  # Regresar a la rama principal
  git switch main

  # Fusionar la rama de desarrollo
  git merge nueva-funcion
  ```

---

## 📚 Fuentes y Referencias

* [Git SCM - Ramificaciones en Git](https://git-scm.com)
* [Atlassian Git Tutorials - Git Merge](https://atlassian.com)
