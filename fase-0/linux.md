# Guía Rápida de Comandos Esenciales de Linux

Una guía práctica con la definición y un ejemplo de uso para los comandos y herramientas más importantes de la terminal de Linux.

---

## 1. `cd` (Change Directory)
* **Qué es:** Es el comando utilizado para **cambiar de directorio** (carpeta) actual en la terminal. Te permite moverte a través de la estructura de archivos del sistema.
* **Ejemplo:**
  ```bash
  cd /var/www/html
  ```
  *(Este comando te traslada directamente a la carpeta `html` ubicada en la ruta absoluta especificada. Si escribes solo `cd` sin ruta, te regresa a tu directorio personal o Home).*

---

## 2. `ls` (List)
* **Qué es:** Permite **listar los archivos y carpetas** que se encuentran dentro del directorio actual. Es ideal para ver qué contenido hay disponible.
* **Ejemplo:**
  ```bash
  ls -la
  ```
  *(Muestra una lista detallada `-l` de todos los archivos, incluyendo los ocultos que empiezan con un punto `-a`, junto con sus permisos, tamaño y fecha de modificación).*

---

## 3. `grep` (Global Regular Expression Print)
* **Qué es:** Es una potente herramienta de búsqueda por **expresiones regulares**. Sirve para buscar cadenas de texto específicas dentro de archivos o en la salida de otros comandos.
* **Ejemplo:**
  ```bash
  grep "error" /var/log/syslog
  ```
  *(Busca y muestra en pantalla todas las líneas del archivo `/var/log/syslog` que contengan la palabra "error").*

---

## 4. `cat` (Concatenate)
* **Qué es:** Se utiliza principalmente para **leer, mostrar o concatenar** el contenido de archivos de texto directamente en la terminal sin necesidad de abrir un editor de texto.
* **Ejemplo:**
  ```bash
  cat archivo.txt
  ```
  *(Imprime en la pantalla todo el texto contenido dentro de `archivo.txt`).*

---

## 5. `chmod` (Change Mode)
* **Qué es:** Modifica los **permisos de lectura, escritura y ejecución** de un archivo o directorio para los diferentes usuarios (propietario, grupo y otros).
* **Ejemplo:**
  ```bash
  chmod +x script.sh
  ```
  *(Le otorga permisos de ejecución `+x` al archivo `script.sh` para que pueda correr como un programa).*

---

## 6. Pipes (`|`)
* **Qué es:** No es un comando por sí mismo, sino un **conector** (representado por la barra vertical `|`). Su función es tomar la salida generada por un comando y enviarla directamente como entrada a otro comando.
* **Ejemplo:**
  ```bash
  ls -la | grep ".txt"
  ```
  *(Primero lista todos los archivos de la carpeta actual y, mediante el pipe, pasa esa lista a `grep` para que este último filtre y muestre únicamente los archivos que terminan en `.txt`).*

---

## 7. `cron`
* **Qué es:** Es el **administrador de procesos en segundo plano** (demonio) en sistemas Unix/Linux que se encarga de **automatizar tareas** programadas para que se ejecuten en fechas y horas específicas.
* **Ejemplo:**
  Para configurar estas tareas se utiliza el editor de la tabla de tareas (`crontab -e`). Una línea típica de configuración sería:
  ```bash
  0 3 * * * /ruta/al/script/respaldo.sh
  ```
  *(Esta instrucción le indica al sistema que ejecute automáticamente el script de respaldo `respaldo.sh` todos los días exactamente a las 3:00 a. m.).*
