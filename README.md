# 📌 Configuración del Proyecto con Docker

Este documento proporciona las instrucciones detalladas para:
- Descargar la API desde Git
- Construir la imagen de Docker
- Ejecutar el contenedor

---

## 📥 1. Creación de red

### 🔹 Creamos una red si no existe
```sh
docker network create dev-red

```

---

## 🔄 2. Descargar la API desde GitHub

Clona el repositorio:
```sh
git clone https://github.com/orenarounicesar/devops202501-html.git
cd devops202501-html

```

---

## 🐳 3. Construcción de la Imagen Docker

2️⃣ Construye la imagen:
```sh
docker build . -t devapp

```

---

## 🚀 4. Ejecutar los Contenedores con Docker

### 🔹 Ejecución:
```sh
docker run -d --name dev-app --network=dev-red -p 3000:3000 devapp

```

---

## 📝 5. Verificación de Contenedores en Ejecución

```sh
docker ps

```

Si todo está bien, verás los contenedores `dev-app` en ejecución.


---

## 📝 6. Verificación en el Navegador

```sh
http://localhost:3000
```

---