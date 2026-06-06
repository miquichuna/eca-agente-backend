# GEMA — Backend del agente conversacional
## Proyecto ECA · Guía de Planos y Movimientos de Cámara

Este es el servidor que conecta el chat del agente GEMA con la API de Claude (Anthropic).
Protege la API key para que los usuarios no puedan verla.

---

## Cómo desplegarlo en Render (paso a paso)

### 1. Sube esta carpeta a GitHub
- Crea un repositorio nuevo en github.com (ej: `eca-agente-backend`)
- Sube todos estos archivos

### 2. Crea una cuenta en Render
- Ve a render.com y regístrate (gratis)
- Elige "New Web Service"
- Conecta tu cuenta de GitHub y selecciona el repositorio `eca-agente-backend`

### 3. Configura el servicio
- **Name:** eca-agente-backend
- **Runtime:** Node
- **Build Command:** `npm install`
- **Start Command:** `npm start`
- **Plan:** Free

### 4. Añade la variable de entorno
- En la sección "Environment Variables" añade:
  - **Key:** `ANTHROPIC_API_KEY`
  - **Value:** (tu API key de Anthropic)

### 5. Despliega
- Haz clic en "Create Web Service"
- Render te dará una URL tipo: `https://eca-agente-backend.onrender.com`
- Guarda esa URL — la necesitarás en el HTML de la guía

---

## Para "cortar el grifo"
Si quieres que el agente deje de funcionar (para no gastar créditos):
- Ve a Render → tu servicio → "Suspend Service"
- O simplemente no recargues créditos en Anthropic Console

---

## Coste estimado
Cada conversación con GEMA cuesta aproximadamente 0,001€ - 0,003€.
Con un uso de evaluación (pocos correctores, pocas preguntas), el gasto total será inferior a 0,50€.
