# Visualizador de Boletines

Página web sencilla para subir PDFs de boletines de servicio técnico y visualizar los avisos extraídos por un workflow de **n8n**.

## Uso

1. Abre `index.html` (o `boletines-n8n.html`) en el navegador, o activa **GitHub Pages**.
2. Pega la URL de tu webhook de n8n (ej. `https://tu-n8n.com/webhook/boletines`).
3. Arrastra o selecciona el PDF del boletín.
4. Pulsa **Procesar PDF**.

También puedes usar **Cargar datos de ejemplo** para ver la interfaz sin n8n.

## Requisitos en n8n

- Nodo **Webhook** (POST) con `binaryPropertyName: data`
- Conectado a **Extract From File** (PDF) y el resto de tu flujo de extracción
- Termina en **Respond to Webhook** devolviendo los avisos (formato plano `columnaA`/`columnaB` o JSON estructurado)

## GitHub Pages

Settings → Pages → Source: Deploy from branch → `main` → `/ (root)`.

La web quedará en: `https://f1r0x.github.io/Visualizador-de-Boletines/`
