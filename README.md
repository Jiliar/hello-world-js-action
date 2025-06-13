# 🚀 Hello World JS GitHub Action

Esta es una acción de GitHub creada con **Node.js**, diseñada como ejemplo básico para saludar a un usuario y mostrar la hora actual.  
Ideal como punto de partida para crear y publicar tus propias acciones personalizadas en el **GitHub Actions Marketplace**.

---

## 📦 ¿Qué hace esta acción?

- Recibe un nombre como entrada (`who-to-greet`)
- Imprime un saludo en los logs
- Genera la hora actual y la devuelve como salida (`time`)
- Muestra el payload del evento que activó el workflow

---

## 🧪 Ejemplo de uso

```yaml
name: Ejemplo de uso de Hello World JS Action

on: [push]

jobs:
  greet:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout del código
        uses: actions/checkout@v4

      - name: Ejecutar saludo
        uses: Jiliar/hello-world-js-action@v1.0
        with:
          who-to-greet: 'Mundo'