# ET_VisionA


## **1. Investigación y referentes**

El proyecto surge del interés compartido de **Sebastián Pedroza** y **Ricardo Guerrero** por la película ***E.T. El Extraterrestre* (Steven Spielberg, 1982)**, una obra que marcó su infancia y que combina la ciencia ficción con la emotividad del vínculo entre un niño y un ser de otro mundo.
A partir de esta inspiración, se buscó trasladar la simbología del **dedo luminoso de E.T.**, que representa conexión, empatía y sanación, hacia un entorno interactivo creado con **visión artificial**.

Para lograrlo, se utilizó la técnica de **detección de manos (HandPose)** a través de la librería **ml5.js**, que permite rastrear en tiempo real los puntos clave de la mano humana. Esta técnica sirvió como base para recrear el gesto icónico del contacto entre E.T. y el niño, pero ahora dentro de un universo digital en el que la unión de los dedos **genera vida, planetas y energía**.

Como referentes técnicos y artísticos se tuvieron en cuenta:

* **“Augmented Hand Series”** – *Golan Levin, Chris Sugrue y Kyle McDonald (2014)*: instalación interactiva que transforma digitalmente las manos del usuario en criaturas mutantes, explorando la identidad y la extensión del cuerpo mediante visión artificial.
* **“Hand Tracking with ml5.js – Interactive Gestures”** – ejemplos comunitarios en *The Coding Train* y *ml5.js demos*, donde la posición del dedo índice se usa como punto de control en entornos creativos.
* **“Air Drawing – Gesture-Based Art Creation”** (2023): proyectos donde la unión o separación de los dedos genera trazos o efectos visuales en el aire, concepto base para el gesto de “crear planetas” en esta experiencia.

Estos referentes muestran cómo la visión artificial puede integrarse en prácticas artísticas y emocionales, no solo como herramienta técnica sino como **medio simbólico de conexión entre humanos y tecnología**.

---

##  **2. Diseño conceptual **

El concepto central del proyecto se titula **“Creación Cósmica: E.T. Connection”**, una experiencia interactiva inspirada en el vínculo entre **E.T. y Elliott**, donde los gestos de las manos de dos personas se convierten en el motor de la creación de un universo.

La experiencia invita a **jugar en pareja**, evocando la complicidad de los protagonistas de la película. Al unir los dedos índices, como en la escena icónica del toque luminoso, **se genera energía cósmica**, dando origen a planetas y constelaciones.
El **universo visual** (planetas girando, partículas de luz, la Luna como destino final) remite a los elementos más simbólicos de la película: la bicicleta volando frente a la luna y la sensación de ascenso hacia algo más grande y trascendente.

El diseño busca **equilibrar lo emocional con lo sensorial**, convirtiendo el gesto en una metáfora de unión y creación compartida.
La interfaz gestual transforma la pantalla en un espacio poético, donde **la amistad, la colaboración y la curiosidad científica** se materializan en forma de luz y movimiento.

---

##  **3. Planificación técnica **

El desarrollo del proyecto se planteó en tres fases principales, siguiendo una estructura que combina narrativa, interacción y progresión visual:

1. **Fase Solar – Creación de Planetas:**
   Se utiliza el modelo **ml5.handpose** para detectar las manos de ambos participantes. Cuando los índices se acercan, se activa un evento visual que genera un nuevo planeta, acompañado por un destello de luz o energía.

2. **Fase E.T. – El Vuelo y los Obstáculos:**
   Se recrea el recorrido del niño y E.T. volando hacia la Luna. El jugador controla el movimiento a través de la distancia entre los dedos, y debe evitar obstáculos mientras mantiene el equilibrio.

3. **Fase Ascensión – Llegada a la Luna:**
   Una secuencia final donde los planetas orbitan y la Luna aparece como símbolo de logro y unión. Se aplican efectos de transición suave (fade in / fade out) para dar una sensación de calma y cierre.

El sistema está implementado con **JavaScript**, **p5.js** y **ml5.js**, usando una **detección en tiempo real de puntos clave de la mano**.
La estructura modular del código permite ajustar fácilmente niveles, efectos o fases.
Técnicamente es viable en cualquier navegador con cámara, y conceptualmente apuesta por **integrar tecnología, narrativa y emoción** en una misma experiencia.

---

¿Quieres que te lo deje en **formato informe (listo para entregar en Word o PDF)** con portada, subtítulos y una cita corta tipo APA al final?
Puedo hacerlo en menos de un minuto con diseño limpio y lista la parte escrita.
