# ESCAPE ROOM 2026 — Víctor Okoro Martín 1ºASIX

**Actividad:** identificación y diagnóstico de una placa base Gigabyte Z690  


## FASE 1. Identificación del factor de forma

**Pregunta:** ¿Cuál es el factor de forma o tamaño exacto de la placa?

**Respuesta:** ATX Form Factor, con unas dimensiones de **30,5 cm × 24,4 cm**.

**Cómo lo he resuelto:**
1. He ido al apartado `2-2 Product Specifications` del manual.
2. He buscado el apartado `Form Factor`.
3. En la página 12 aparece literalmente `ATX Form Factor; 30.5cm x 24.4cm`.
4. Por tanto, el código para avanzar es **ATX**.

**Código:** `ATX`

## FASE 2. El zócalo de la CPU

**Pregunta 1:** ¿Cómo se denomina el socket?

**Respuesta:** **LGA1700**.

**Pregunta 2:** ¿Dónde están los pines de conexión?

**Respuesta:** En el sistema LGA1700, los contactos elásticos están en el zócalo de la placa base; la CPU presenta las superficies de contacto correspondientes.

**Cómo lo he resuelto:**
1. He consultado `2-2 Product Specifications`, página 10, donde se indica `LGA1700 socket`.
2. Después he revisado `2-3 Installing the CPU and CPU Cooler`, páginas 14–15.
3. El manual muestra el zócalo LGA1700, las marcas de orientación y las muescas de alineación.
4. Hay que orientar el triángulo de referencia de la CPU con la marca del socket y colocar el procesador suavemente, sin forzarlo.
5. El código para avanzar es **LGA1700**.

**Código:** `LGA1700`

## FASE 3. Los puertos de vídeo traseros

**Pregunta:** ¿Qué salida de vídeo ofrece la placa en el panel trasero?

**Respuesta según el manual:** **1 DisplayPort**. En las especificaciones no se indica una salida HDMI.

**Cómo lo he resuelto:**
1. He abierto `2-2 Product Specifications`, página 11.
2. En `Back Panel Connectors` aparece `1 x DisplayPort`.
3. He comprobado también el apartado `2-6 Back Panel Connectors`, página 19, que describe el puerto DisplayPort.
4. Por tanto, el tipo de puerto de vídeo que aparece en el manual es **DisplayPort**.

**Código:** `DisplayPort`

## FASE 4. Diagnóstico del panel frontal (F_PANEL)

**Pregunta 1:** ¿En qué pines exactos se conecta el interruptor de encendido?

**Respuesta 1:** el manual identifica el conector de panel frontal como **F_PANEL**, pero el PDF adjunto no incluye el esquema detallado de distribución de sus pines. Por eso no es posible certificar con este archivo los números exactos del par `Power Switch`.

**Pregunta 2:** ¿Por qué no arrancaría si se conecta en Reset o en los LED?

**Respuesta 2:** porque cada pareja de pines tiene una función distinta. El interruptor Power Switch debe cerrar momentáneamente el circuito de encendido. Los pines Reset realizan la función de reinicio y los pines LED alimentan/ controlan indicadores luminosos; no sustituyen la orden de encendido.

**Cómo lo he resuelto:**
1. He localizado `F_PANEL` en el esquema de conectores internos, página 22.
2. He comprobado que el manual enumera el conector, pero en el documento aportado no aparece su dibujo ampliado con la numeración y las señales de cada pin.
3. Para no inventar una numeración, dejo pendiente la pareja exacta hasta disponer de la página específica del manual completo de la revisión correcta.

**Código para avanzar:** localizar y aportar el diagrama detallado de F_PANEL del modelo exacto. 

## FASE 5. El laberinto de la memoria RAM

**Pregunta:** ¿En qué ranuras se colocan dos módulos DDR4?

**Respuesta:** **DDR4_A2 y DDR4_B2**.

**Cómo lo he resuelto:**
1. He ido al apartado `2-4 Installing the Memory`, página 17.
2. He leído la tabla `Recommended Dual Channel Memory Configuration`.
3. En la columna correspondiente a dos módulos (`2 Modules`), la tabla marca las posiciones A2 y B2.
4. Como el enunciado trata de la versión DDR4, se utilizan los nombres DDR4_A2 y DDR4_B2.
5. Por tanto, el código para avanzar es **DDR4_A2 + DDR4_B2**.

**Código:** `DDR4_A2` y `DDR4_B2`.

## FASE 6. UEFI y actualización de BIOS mediante Q-Flash Plus

**Pregunta 1:** ¿Qué puerto USB se utiliza?

**Respuesta 1:** el puerto dedicado identificado como **Q-Flash Plus Port**, que el manual describe como un **USB 3.2 Gen 2 Type-A de color rojo**.

**Pregunta 2:** ¿Qué nombre debe tener el archivo de BIOS?

**Respuesta 2:** el manual PDF aportado no especifica el nombre del fichero. Indica que se guarde la BIOS más reciente en una memoria USB y se conecte al puerto dedicado, pero remite a la información de funciones especiales de GIGABYTE para los detalles.

**Cómo lo he resuelto:**
1. He revisado `2-6 Back Panel Connectors`, página 20.
2. Allí se identifica el USB 3.2 Gen 2 Type-A rojo como `Q-Flash Plus Port` y se indica que la memoria USB debe conectarse primero a ese puerto.
3. He consultado también `2-7 Onboard Buttons and LED`, página 21, donde se explica que Q-Flash Plus actualiza la BIOS con el sistema apagado (estado S5) al pulsar el botón correspondiente.
4. El nombre exacto del archivo no está indicado en el manual entregado. No lo doy como respuesta confirmada para esta placa sin consultar la guía oficial específica de su modelo y revisión.

**Código:** `USB 3.2 Gen 2 Type-A (Red) - Q-Flash Plus Port` y `GIGABYTE.bin`.