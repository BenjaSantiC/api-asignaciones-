# API de Asignación de Personal para Planes Digitales 🚀

Esta API está diseñada para automatizar la asignación de personal a proyectos digitales según la demanda de planes (Plata, Gold, Platinum). Fue creada como parte del sistema operativo de **Impulsa Digital** y se conecta con **Excel Online + Power Apps** a través de Power Automate.

---

## ⚙️ Funcionalidades

- 🧠 Verifica disponibilidad de horas por profesional.
- ✅ Asigna binariamente a los roles requeridos por cada plan.
- 🚫 Rechaza asignaciones si algún profesional excede las 160 h/mes.
- 🔁 Reinicia ocupación cada 1° del mes automáticamente.
- 📊 Calcula cuántos planes aún pueden ser tomados en el mes.
- 📥 Entrada: Excel Online con ocupación actual.
- 📤 Salida: Matriz binaria por proyecto y disponibilidad mensual.

---

## 📂 Estructura del Excel

- **Hoja `Ocupación`**: contiene horas acumuladas por profesional.
- **Hoja `Asignaciones`**: matriz binaria de asignación por proyecto.
- **Hoja `Disponibilidad`**: cuántos planes pueden asignarse.

---

## 🚀 ¿Cómo desplegar?

1. Subir este repositorio a GitHub.
2. Crear un Web Service gratuito en [Render.com](https://render.com).
3. Usar este comando de ejecución:
   ```bash
   uvicorn main:app --host 0.0.0.0 --port 10000
