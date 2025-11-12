
# **Proyecto Final: Visión Artificial**

## **Título:** *ET: Rumbo a Casa*
## [Ver prototipo interactivo en p5.js](https://editor.p5js.org/arturito745/full/WF90umiLL)

**Integrantes:** Sebastián Pedroza y Ricardo Guerrero

---

## **Presentación del proyecto**

El proyecto **“ET: Rumbo a Casa”** surge a partir de un interés compartido por la película *E.T. el Extraterrestre*, un clásico del cine que marcó a ambos integrantes. Sebastián Pedroza y Ricardo Guerrero decidieron tomar como inspiración la conexión emocional entre el niño y el alienígena, y especialmente la icónica escena en la que **E.T. ilumina su dedo** para sanar.

A partir de esa idea, se escogió trabajar con la técnica de **visión artificial HandPose** (detección de la posición de los dedos), como una forma simbólica de recrear ese contacto entre ambos personajes, pero ahora desde la interacción humano-computador.

La experiencia está pensada para **dos personas**: cada jugador controla una mano frente a la cámara, y a través del movimiento y cercanía de sus dedos índices, se activa una serie de transiciones visuales que representan **la unión, la creación y el viaje hacia el cosmos**, reflejando la amistad y el vínculo que caracterizan la película.

El universo, las estrellas y la luna son elementos esenciales, pues en *E.T.* el cielo nocturno es símbolo de hogar, distancia y reencuentro. Por eso, la **luna** tiene un papel central en el diseño visual del proyecto.

---

## **Etapa de Diseño**

### **Investigación y referentes**

El referente principal es la **película *E.T. el Extraterrestre*** (Steven Spielberg, 1982), de donde se toma la metáfora del dedo que brilla como conexión entre mundos.
Desde lo técnico, se explora el uso del modelo **ml5.js HandPose**, basado en MediaPipe, para detectar las posiciones de los dedos y generar respuestas visuales interactivas.

El enfoque artístico se orienta hacia **crear una experiencia sensorial y colaborativa**, donde los usuarios generan energía cósmica y forman una luna a partir de sus movimientos. La unión de ambas manos activa procesos visuales como **explosiones de partículas, formaciones lunares y transiciones suaves (fade in / fade out)** .

[![Escena clásica de ET](https://img.youtube.com/vi/gTVoFCP1BLg/0.jpg)](https://www.youtube.com/watch?v=gTVoFCP1BLg)

[![Interacción con visión artificial y handpose](https://img.youtube.com/vi/yn_Bg0ps0d8/0.jpg)](https://www.youtube.com/watch?v=yn_Bg0ps0d8)

[![Demo del proyecto](https://img.youtube.com/vi/5uKmLMo0OlY/0.jpg)](https://youtu.be/5uKmLMo0OlY?si=PB6OpiBEiE8Vusbl)

---

### **Diseño conceptual**

El proyecto se divide en tres fases que narran un **viaje simbólico**:

1. **Inicio:** Los jugadores deben unir sus dedos índices para iniciar la conexión y comenzar la experiencia.
2. **Fase Solar (creación lunar):** Al acercar los dedos, se generan esferas de energía que poco a poco forman una **luna compuesta por partículas**, simbolizando la creación conjunta.
3. **Fase ET (vuelo):** Inspirada en la escena de la bicicleta voladora, el jugador controla con sus dedos la altura de E.T. y su amigo, esquivando obstáculos mientras se dirigen hacia la luna.
4. **Ascensión:** Una escena final donde la luna brilla y el universo se reinicia.

Cada una de estas etapas combina **interacción corporal y narrativa visual**, integrando elementos como partículas, gradientes y efectos de luz. El diseño busca transmitir **emoción, colaboración y nostalgia**, más allá de una simple detección técnica.

---

### **Planificación técnica**

El proyecto fue implementado en **p5.js** con la librería **ml5.handPose()**, integrando detección de manos en tiempo real a través de la cámara.
Desde el código base, se desarrollaron distintas funcionalidades personalizadas:

* **Reconocimiento de manos izquierda y derecha:**

  ```js
  function identifyHands() {
    handLeft = null;
    handRight = null;
    if (hands.length >= 2) {
      hands.sort((a, b) => a.keypoints[0].x - b.keypoints[0].x);
      handRight = hands[0];
      handLeft = hands[1];
    }
  }
  ```

* **Transición entre fases (fade in / fade out):**
  Uno de los principales retos técnicos fue implementar transiciones suaves para que el cambio de escenas se sintiera fluido.

  ```js
  function startFadeTransition(nextState, type) {
    fadeAlpha = type === "in" ? 255 : 0;
    fadeType = type;
    fadeInProgress = true;
    fadeSpeed = 5;
  }
  ```

* **Formación de la luna con partículas:**
  Este fue uno de los ajustes más significativos, ya que originalmente el sistema era solar, pero se transformó en una **luna hecha de partículas** que emergen de la energía creada por las manos.

  ```js
  function startMoonFormation() {
    moonFormation = true;
    for (let i = 0; i < 100; i++) {
      moonParticles.push({
        x: random(width),
        y: random(height),
        targetX: width/2,
        targetY: height/2
      });
    }
  }
  ```

**Distribución del trabajo:**

* *Sebastián Pedroza:* diseño visual, efectos de partículas, creación de la luna y pruebas estéticas.
* *Ricardo Guerrero:* estructura general del código, transiciones entre fases y control del movimiento con distancia entre dedos.
  Ambos trabajaron en conjunto en la calibración del modelo HandPose y la dirección creativa.

**Principales retos:**

* Lograr una detección estable con dos manos en simultáneo.
* Sincronizar los eventos visuales según la distancia entre dedos.
* Mantener una estética coherente con el universo de *E.T.*
* Implementar las **transiciones con fade** sin romper el flujo del sketch.

---

## **Etapa de Implementación (60%)**

### **Funcionamiento técnico (25%)**

El proyecto integra correctamente la detección de manos y el cálculo de distancia entre dedos índices para controlar la experiencia. La lógica de fases, la creación de partículas y la física básica del movimiento fueron implementadas con éxito.

El código se optimizó para funcionar en tiempo real, priorizando la fluidez visual sobre la complejidad gráfica.

### **Calidad visual**

El lenguaje visual se inspira en el **universo nocturno de E.T.**, con tonos oscuros, brillos, explosiones suaves y partículas flotantes. La formación de la luna representa el clímax visual del proyecto.

El uso de gradientes, halos y luces dinámicas genera una atmósfera inmersiva y cinematográfica.

### **Integración e interacción**

El proyecto logra una interacción simbólica y emocional: dos personas deben **cooperar** para avanzar, reflejando el vínculo de la película.
El sistema responde a los movimientos de las manos en tiempo real, generando una sensación de conexión viva entre los usuarios y el entorno visual.

---

## **Conclusión**

“ET: Rumbo a Casa” combina tecnología, narrativa y emoción en una experiencia interactiva que busca reconectar al espectador con el asombro infantil y la magia de la colaboración.
La unión de la visión artificial y el arte digital permitió construir una historia visual donde el gesto humano se convierte en puente entre mundos.


