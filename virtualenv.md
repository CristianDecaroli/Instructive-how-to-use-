### 📌 **Guía Completa: Uso de `virtualenv` en Windows con PowerShell**  

Si querés usar `virtualenv` en Windows con PowerShell, seguí estos pasos.  

---

## 🔹 **1. Instalar `virtualenv` (si no lo tenés)**  
Abrí **PowerShell** y ejecutá:  
```sh
pip install virtualenv
```
Verificá que se instaló correctamente con:  
```sh
virtualenv --version
```

---

## 🔹 **2. Crear un entorno virtual**  
### ✅ **Opción 1: Usar la versión actual de Python**  
Si querés usar la misma versión de Python con la que estás trabajando, creá el entorno en la carpeta del proyecto:  
```sh
virtualenv venv
```
Esto generará una carpeta llamada `venv` con el entorno virtual.

### ✅ **Opción 2: Elegir una versión específica de Python**  
Si tenés varias versiones de Python instaladas, podés especificar cuál usar:  
```sh
virtualenv -p C:\Ruta\A\Python39\python.exe mi_entorno
```
Ejemplo si tenés Python 3.9 en `C:\Python39`:  
```sh
virtualenv -p C:\Python39\python.exe venv
```

---

## 🔹 **3. Activar el entorno virtual en PowerShell**  
Para activar el entorno virtual, usá este comando dentro de la carpeta del proyecto:  
```sh
.\venv\Scripts\Activate
```
Si ves algo como `(venv) PS C:\mi_proyecto>` al inicio de la línea, significa que el entorno está activado. ✅  

### ❗ **Si aparece un error de ejecución de scripts (`Execution Policy`)**  
Si PowerShell te da un error de seguridad, ejecutá:  
```sh
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
Luego, intentá activar el entorno otra vez.

---

## 🔹 **4. Instalar dependencias desde `requirements.txt`**  
Si ya tenés un archivo `requirements.txt` con las librerías necesarias, instalalas con:  
```sh
pip install -r requirements.txt
```

---

## 🔹 **5. Verificar paquetes instalados**  
Para ver qué paquetes están instalados en tu entorno virtual:  
```sh
pip list
```

---

## 🔹 **6. Desactivar el entorno virtual**  
Cuando termines de trabajar, desactivá el entorno con:  
```sh
deactivate
```

---

## 🔹 **7. Eliminar el entorno virtual**  
Si querés borrar el entorno virtual, simplemente eliminá la carpeta:  
```sh
Remove-Item -Recurse -Force venv
```
Después de esto, podés crear uno nuevo si lo necesitás.

---

### 🚀 **Resumen rápido de comandos útiles**
```sh
pip install virtualenv                     # Instalar virtualenv
virtualenv venv                            # Crear un entorno virtual
virtualenv -p C:\Python39\python.exe venv  # Crear entorno con versión específica
.\venv\Scripts\Activate                    # Activar entorno en PowerShell
pip install -r requirements.txt            # Instalar dependencias
pip list                                   # Ver paquetes instalados
deactivate                                 # Desactivar el entorno virtual
Remove-Item -Recurse -Force venv           # Eliminar el entorno virtual
```

Con esto ya tenés `virtualenv` funcionando perfectamente en **Windows con PowerShell**. 🚀🔥