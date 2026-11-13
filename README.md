# Simulador Unidad de Control ALU de 5 bits (CI 7473)

Simulador interactivo estilo **Proteus ISIS** desarrollado en HTML5/SVG/JavaScript autocontenido (sin dependencias externas) para la **Actividad Evaluativa #2** de *Arquitectura del Computador Aplicada* (UCAB).

## Características Principales
- **Registros Síncronos (CI 7473):** Tres Flip-Flops JK (`Q2`, `Q1`, `Q0`) disparados por flanco de bajada (`CLK ↓`), con alimentación `VCC (+5V)`, `GND` y reinicio asíncrono activo en bajo (`CLR' = 0`).
- **Lógica de Excitación (`7404` / `7408`):**
  - $J_2 = \text{INT} \cdot Q_1 \cdot Q_0$, $K_2 = \text{INT}$
  - $J_1 = \text{INT} \cdot Q_0$, $K_1 = \text{INT} \cdot Q_0$
  - $J_0 = \text{INT} \cdot \overline{Q_2}$, $K_0 = \text{INT}$
- **Decodificador y Display de 7 Segmentos de Ánodo Común (`0 = ON`):** Muestra `I` (Inactivo `000`), `S` (Suma `001`), `r` (Resta `010`), `P` (Producto `011`) y `d` (División `100`).
- **Inyección de Ruido Eléctrico:** Permite forzar los estados no válidos `101`, `110` y `111` para comprobar la autorrecuperación (*self-starting*) en un único ciclo de reloj cuando `INT = 1`.
- **Exportación de Evidencia:** Genera capturas PNG de alta resolución con encabezado etiquetado listo para el informe.

## Uso Local o Publicación en GitHub Pages
1. Abre `index.html` directamente en cualquier navegador (Vivaldi, Firefox, Chromium) sin necesidad de servidor.
2. Para subirlo a GitHub:
   ```bash
   git init
   git add .
   git commit -m "feat: simulador unidad de control ALU 5 bits (CI 7473)"
   git branch -M main
   git remote add origin <URL_DE_TU_REPO_GITHUB>
   git push -u origin main
   ```
