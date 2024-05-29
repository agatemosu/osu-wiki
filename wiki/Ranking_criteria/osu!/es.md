# Criterios de clasificación de osu!

***Aviso: Este artículo es una extensión de los [criterios de clasificación generales](/wiki/Ranking_criteria).***

Este conjunto de **criterios de clasificación de osu!** establece [reglas y pautas](/wiki/Ranking_criteria#general-terms) que los [beatmaps](/wiki/Beatmap) específicos de [osu!](/wiki/Game_mode/osu!) deben seguir para avanzar en el [procedimiento de clasificación de beatmaps](/wiki/Beatmap_ranking_procedure).

## Universal

Las reglas y pautas generales se aplican a todo tipo de dificultad de osu!. Las reglas y pautas relacionadas con el ritmo se aplican a beatmaps de aproximadamente 180 BPM con compases de 4/4. Si tu canción es drásticamente más rápida o más lenta, algunas variables pueden ser diferentes, como se detalla en [Escalado de BPM en los criterios de clasificación](/wiki/Ranking_criteria/Scaling_BPM).

### General

#### Reglas

- **Los objetos nunca deben estar fuera de la pantalla en las relaciones de aspecto 4:3.** Los objetos que estén incluso parcialmente fuera de la pantalla pueden crear dificultades de lectura. Prueba a jugar tu beatmap para confirmarlo.
- **Los spinners deben ser lo suficientemente largos para que Auto pueda conseguir 1000 puntos de bonificación.** Los spinners más cortos no permiten un tiempo de giro adecuado.
- **Cada beatmap debe usar al menos dos colores de combo diferentes a no ser que la skin por defecto sea usada.** Los colores del combo deben no mezclarse con el fondo/storyboard/vídeo del beatmap en ningún caso. Esto es para que los objetos estén siempre visibles para el jugador y para que los colores de combo de las skins no se mezclen con el fondo accidentalmente.
- **Todas las partes de los objetos activamente pulsadas deben tener al menos un [hitsound](/wiki/Beatmapping/Hitsound) que no se mezcle con la canción.** Por lo demás, los jugadores no reciben suficiente feedback. No está permitido, por ejemplo, usar [keysounds](/wiki/Beatmapping/Hitsound#keysound) como hitnormals sin otros hitsounds adicionales.
- **Las dificultades se deben convertir a otros modos de juego sin romper la clasificación por estrellas ni los puntos de rendimiento.** En ciertos casos, un archivo `.osu` se puede haber formateado incorrectamente, causando dificultades convertidas a mostrar incorrectamente la clasificación por estrellas y otorgar puntos de rendimiento inexactos.
- **Si el [tiempo de drenaje](/wiki/Beatmap/Drain_time) de cada dificultad es...**
  - **... menos de 3:30**, la dificultad más baja no puede ser más difícil que un Normal.
  - **... entre 3:30 y 4:15**, la dificultad más baja no puede ser más difícil que un Hard.
  - **... entre 4:15 y 5:00**, la dificultad más baja no puede ser más difícil que un Insane.
  - **Los [descansos](/wiki/Beatmap/Break) se pueden combinar con [tiempo de drenaje](/wiki/Beatmap/Drain_time) para cumplir los umbrales anteriores.** Para la dificultad más alta, esto se limita a un máximo de 30 segundos de descanso. Esto no se aplica a las dificultades con menos de 30 segundos de tiempo de drenaje.

#### Pautas

- **Los sliderends que no se representan con un sonido en específico en la música deberían ser [ajustados](/wiki/Beatmapping/Snapping) de acuerdo con la estructura del compás de la canción.** Si la canción usa un compás cuaternario, se debe usar 1/4, 1/8, 1/16. Si la canción usa un compás ternario, se debe usar 1/6 o 1/12. Si la canción tiene un pulso en una posición diferente a la recomendada, el ajuste a un ritmo adecuado siempre tendrá prioridad.
- **Todos los círculos y slider heads deberían estar [ajustados](/wiki/Beatmapping/Snapping) para distinguirlos de los sonidos en la música.** Añadir objetos cuando no hay ninguna pista musical que los justifique puede dar lugar a ritmos desajustados.
- **La [tasa de marcas del slider](/wiki/Beatmapping/Slider_tick_rate) debe ajustarse según la canción.** Por ejemplo, si tu canción contiene una sección que solo usa ritmos de 1/3, no sería adecuado usar la tasa de marcas de 2 para todo el beatmap. En estos casos, se debe utilizar la tasa de marcas de 1.
- **Evita usar colores del combo, bordes del slider o superposiciones del círculo con una luminosidad de ~50 o inferior.** Los colores oscuros como estos afectan a la legibilidad de los círculos de aproximación con poca luz de fondo y los demás elementos renuncian parcialmente a sus funciones como bordes.
- **Evita usar colores del combo y colores del camino del slider con una luminosidad de ~220 o superior durante los kiai time.** Crean pulsos brillantes que pueden resultar desagradables para los ojos.
- **El final de los spinners, el final de los sliders, y los sliders inversos deben dar feedback con hitsounds.** Si se usan para representar un sonido mantenido y no se alinean con un sonido distinto, es aceptable que no den feedback.
- **Evita usar muestras de sonido para sliderslide, sliderwhistle y spinnerspin que no se repitan de forma natural.** Estos hitsounds son continuos, lo que significa que sus archivos se reproducen de principio a fin y en bucle como un sonido continuo durante toda la duración del objeto, por lo que usar archivos de sonido con un impacto claro para ellos podría provocar efectos secundarios no deseados.
- **Evita los picos de dificultad injustificados** La dificultad debe ser representativa de la intensidad de la canción.

### Skinning

#### Reglas

- **Los círculos del spinner y sus centros deben ser claramente visibles y estar exactamente centrados.** Esto es para asegurar que los jugadores tengan una ayuda visible que les ayude a girar consistentemente, así como un punto de referencia visual alrededor del cual girar.
- **Hit100 e hit300 deben ser diferentes de los elementos de la skin correspondientes a geki y katu.** Hit300g, hit300k e hit100k indican si los jugadores acertaron perfectamente todos los 300 en un combo.
- **Se debe seleccionar un color personalizado para el borde del slider cuando un beatmap contiene elementos de skin del conjunto de círculos o sliders.** Esto se hace para evitar que el borde por defecto del slider o el borde personalizado de la skin del jugador entren en conflicto con el esquema de color específico del beatmap. Esto se hace añadiendo `SliderBorder: <RGB Value>` bajo la categoría `[Colours]` en un archivo `.osu`.
- **El color del slider body no puede ser demasiado similar al color del borde del slider.** Si ambos colores son demasiado similares entre sí, el elemento del borde del slider pierde su propósito como borde visual del slider. El color del slider body se puede seleccionar añadiendo `SliderTrackOverride: <Valor RGB>` bajo la categoría `[Colours]` en un archivo `.osu`.
- **El color del slider body y el color del borde del slider juntos no deben mezclarse con el fondo o el vídeo de un beatmap.** En ese caso, hacen que los slider paths sean poco claros o ambiguos para leer. Puede ser aceptable que uno se mezcle mientras el otro no.

#### Pautas

- **El uso del nuevo estilo de los spinners no es recomendado.** Solo se puede usar con la Preferred Skin configurada en Default. Las skins que usan SpinnerBackground cambiarán el color de spinner-background.png y eso podría afectar negativamente la apariencia del spinner.Esta configuración no funciona editando la columna `[Colours]` en el archivo `.osu` del beatmap.

## Dificultades específicas

Las reglas y pautas para las dificultades específicas solo se aplican al nivel de dificultad que se indica y, por lo tanto, *no se aplican a **todas** las dificultades de osu!*. Reglas y pautas relacionadas con el ritmo aplican para beatmaps de aproximadamente 180 BPM. Si tu canción es drásticamente más rápida o lenta, algunas variables pueden ser diferentes, como se detalla en [Escalado de BPM en los criterios de clasificación](/wiki/Ranking_criteria/Scaling_BPM).

### Nombre de las dificultades

*Artículo principal: [Nombramiento de las dificultades](/wiki/Ranking_criteria/Difficulty_naming)*

- ![](/wiki/shared/diff/easy-o.png?20211215) Easy
- ![](/wiki/shared/diff/normal-o.png?20211215) Normal
- ![](/wiki/shared/diff/hard-o.png?20211215) Hard
- ![](/wiki/shared/diff/insane-o.png?20211215) Insane
- ![](/wiki/shared/diff/expert-o.png?20211215) Expert

### ![](/wiki/shared/diff/easy-o.png?20211215) Easy

#### Reglas

- **Los objetos separados por 1 pulso o menos deben no [superponerse](/wiki/Beatmapping/Mapping_techniques/Overlap) completamente.**
- **No uses [sliders con flechas inversas que no sigan la trayectoria visible del slider](/wiki/Ranking_criteria/osu!/img/Unintuitive_slider_reverse_arrow.png).** Estas distorsionan la dirección de un slider.
- **Cada slider debe tener una trayectoria de movimiento clara y visible desde el principio hasta el final.** No se pueden usar sliders que se superponen a sí mismos sin bordes claros ni cuyas secciones individuales son ilegibles. La posición final de un slider debe ser clara bajo la suposición de que un jugador tiene una skin que hace que los círculos finales del slider sean completamente transparentes.
