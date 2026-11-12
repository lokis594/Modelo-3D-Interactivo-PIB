# Modelo 3D Interactivo y Simulador Aeroespacial — Prototipo RC / Planeador Propulsado (PIB)

Visor y simulador 3D interactivo de grado de ingeniería desarrollado en **Three.js** y **HTML5** (arquitectura *single-file*, 100 % autónomo y compatible con `file://` y GitHub Pages).

El gemelo digital replica con precisión milimétrica las cotas de los planos CAD (Onshape) y los materiales y texturas del prototipo físico real.

---

## 🛩️ Especificaciones Geométricas y Dimensionales (Escala: 1 unidad Three.js = 1 cm)

* **Envergadura Alar ($b$):** $89,497\text{ cm}$ de punta a punta en el eje transversal $X$ ($89,798\text{ cm}$ de diagonal máxima en planta).
* **Longitud Total del Fuselaje ($L$):** $63,495\text{ cm}$ en el eje longitudinal ($64,070\text{ cm}$ de distancia diagonal máxima).
* **Perfil Alar:** Plano-convexo Clark Y con cuerda total de $12,13\text{ cm}$, división longitudinal entre sección delantera y trasera, y cavidad rectangular interna del larguero visible en las puntas alares.
* **Sistema de Propulsión (M1–M4):** Cuatro motores con hélices bipala de $\varnothing 45\text{ mm}$ ($4,5\text{ cm}$) montados sobre el borde de ataque alar:
  * Motores internos (M2 y M3) a $8,2\text{ cm}$ del fuselaje.
  * Motores externos (M1 y M4) a $24,6\text{ cm}$ del fuselaje.
* **Empenaje:**
  * **Estabilizador Vertical (Deriva):** Base de $43\text{ cm}$ a $63\text{ cm}$ desde la nariz, altura de $11\text{ cm}$ con borde de ataque en flecha.
  * **Estabilizador Horizontal:** Forma trapezoidal simétrica en planta ($53$ a $62\text{ cm}$ en el avión real), alternable con la posición CAD ($+2,7\text{ cm}$ hacia atrás).
* **Puntos Aerodinámicos y Estabilidad Estática:**
  * Borde de Ataque (BA): $21,55\text{ cm}$.
  * Centro Aerodinámico del Ala (CA, 25 % de cuerda): $24,55\text{ cm}$.
  * Centro de Gravedad de Diseño (CG, 40 % de cuerda): $26,40\text{ cm}$.
  * Punto Neutro (PN, Margen Estático $+10,7\text{ \%}$): $27,70\text{ cm}$.

---

## 🎨 Modos de Visualización

1. **Modo Avión Real Físico (por defecto):**
   * Forro verde esmeralda con acabado satinado y textura procedural de pliegues/arrugas.
   * Traslucidez calibrada que permite intuir las 18 costillas y largueros de balsa sin penalización de GPU (60 FPS estables).
   * Estabilizadores en textura de cartón kraft con parches de cinta de enmascarar en la deriva.
   * Lastre de alambre/plomo enrollado en el extremo de la nariz.
2. **Modo Vista CAD Onshape:**
   * Fuselaje y góndolas en azul celeste metálico (`#8ab4d0`).
   * Sección delantera del ala en gris claro (`#d4d6d8`) y trasera en amarillo ocre (`#e59819`).
   * Deriva en azul marino (`#1f3f85`) y estabilizador horizontal en gris medio (`#808487`).

---

## 🔬 Herramientas de Ingeniería y Simulación

* **Modo Rayos X:** Vuelve semitransparente el fuselaje para exponer el lastre de plomo de $14\text{ g}$ ($0$ a $1,5\text{ cm}$), la batería LiPo de $14\text{ g}$ ($4$ a $7\text{ cm}$) y la estructura interna completa del ala.
* **Regla Graduada 3D y Cotas:** Regla continua de $0$ a $63,5\text{ cm}$ y cotas de ingeniería con etiquetas 3D flotantes.
* **Simulación de Actitud:** Control de cabeceo (Pitch), alabeo (Roll) y guiñada (Yaw) pivotando exactamente sobre el Centro de Gravedad ($26,40\text{ cm}$).
* **Modo Demostración:** Oscilación armónica que ilustra la estabilidad estática longitudinal y lateral.
* **Vistas Rápidas:** Vistas ortográficas instantáneas (Planta, Perfil, Frontal) e isométrica 3D libre.
* **Mobile-First & Touch:** Interfaz responsiva con *bottom sheet* desplegable y encuadre automático de cámara para pantallas verticales.

---

## 🚀 Despliegue en GitHub Pages

Para ver el visor 3D directamente en el navegador:
1. Ve a **Settings** > **Pages** en tu repositorio de GitHub.
2. En **Build and deployment** > **Branch**, selecciona `main` (o `master`) y carpeta `/(root)`.
3. Haz clic en **Save**. En unos segundos estará disponible en:
   `https://lokis594.github.io/Modelo-3D-Interactivo-PIB/`
