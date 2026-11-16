# 7th Dragon 2020-II — Traducción al castellano

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Traducción al **castellano de España** de la versión japonesa de PSP de *7th Dragon 2020-II*
(NPJH-50716). Se ha traducido desde el japonés, sin usar el texto de ningún otro parche, y con
la misma terminología que la [traducción de la primera parte](https://github.com/johanderohan/7th-dragon-2020-traduccion-es).

Se distribuye únicamente un **parche xdelta**. Necesitas tu propia copia del juego.

## Estado

**v1.0 — en revisión.** Todo el texto extraído está traducido y revisado, pero no se ha
completado una partida de principio a fin ni existe revisión humana independiente.
La traducción y su revisión están asistidas por IA.

- Historia, conversaciones con los residentes, comunicaciones de las navegantes, encargos,
  menús, objetos, habilidades, enemigos, mensajes de combate, avisos del sistema y tutoriales
  de texto.
- 18.919 cadenas con texto (11.247 distintas): los diálogos de los 179 guiones de evento y las
  tablas de combate, objetos, enemigos, menús, misiones y mapa. Ninguna queda en japonés.
- Fuente nueva con tildes, ñ, ü, signos de apertura y comillas españolas, a tamaño real y con
  los mismos colores que el original.
- 210 texturas redibujadas en 186 archivos: las 15 páginas del resumen «BEFORE STORY» del
  título, los títulos de capítulo, las placas de zona y de mazmorra, los rótulos de los
  minimapas del Parlamento, las órdenes «Usar» y «Tirar», la leyenda del mapa y las barras de
  lugar.
- Voces originales japonesas. Los rótulos gráficos que el juego original ya muestra en inglés
  (menú principal, órdenes de combate, estado) se conservan.

## Cómo aplicar el parche

1. Usa la ISO japonesa **NPJH-50716** que coincida con las huellas de abajo.
2. Aplica `7th.Dragon.2020-II.ES.v1.0.xdelta` con Delta Patcher, xdeltaUI o xdelta3.
3. Comprueba el tamaño y MD5 del resultado. El parche se aplica sobre el original japonés,
   no sobre otro parche.
4. Abre la ISO resultante en PPSSPP o en tu equipo compatible. Solo se ha probado en PPSSPP;
   no se ha comprobado en PSP física ni en PS Vita con Adrenaline.
5. Si tienes instalados los datos del juego japonés (DATA INSTALL), bórralos y vuelve a
   instalarlos con la ISO traducida. No mezcles los datos instalados con otra versión.

```sh
xdelta3 -d -s "7th Dragon 2020-II (Japan).iso" \
  7th.Dragon.2020-II.ES.v1.0.xdelta "7th Dragon 2020-II (Castellano).iso"
```

| Archivo | Tamaño en bytes | MD5 |
|---|---:|---|
| ISO japonesa original | 1.324.154.880 | `f8b2c5c53191e5c6891371c3ed0a129f` |
| ISO resultante v1.0 | 1.324.154.880 | `9c5b66d55df070aa9cbcc3a5952c677c` |

SHA-256 de la ISO resultante: `dd99b9ff2a1632c91ff82b92aa5d9e0e576b787e6214016ef3c8ccd6c97f9670`.

## Comprobaciones

La construcción parte siempre del original y una auditoría lee de nuevo la ISO ya montada:
comprueba cada cadena traducida y cada archivo de texturas contra lo esperado, que el código de
los guiones es idéntico fuera de las cadenas traducidas, que ningún archivo del juego se mueve
ni se solapa con otro, que todo lo que no se ha traducido queda idéntico y en su sitio, y que
no queda texto japonés. El ejecutable original no se ha modificado.

Se ha jugado en el emulador, en tres candidatas sucesivas:

- **Primera candidata** (partida nueva, unas 1.070 capturas): aviso inicial, título, dificultad,
  escena de apertura, creación de personaje, menú completo (objetos, equipo, estado, opciones
  con todos sus valores), conversaciones, elección de navegante, mapa de Tokio, un combate
  completo y la Oficina Murakumo.
- **Segunda candidata** (partida nueva, unas 850 capturas): historia hasta la mazmorra de la
  Sky Tower, varios combates completos con habilidades, objetos y combate automático, subida a
  nivel 2 y 3, fin de partida, y **guardar y cargar una partida**.
- **Candidata publicada:** arranque en frío con partida nueva hasta tomar el control del
  personaje, carga de una partida guardada, menú de objetos, pantalla de estado con sus
  habilidades y un combate completo con su pantalla de resultados.

Otro revisor miró todas las capturas de las dos primeras rondas comparándolas con el original:
sin fallos que impidan jugar ni restos de japonés en el texto. Los defectos de maquetación que
encontró (espacios dobles junto a símbolos y antes de nombres insertados, descripciones de
habilidad deformadas en la pantalla de estado, raya demasiado corta) se corrigieron para la
candidata publicada; de esas correcciones solo se ha visto en pantalla la de las descripciones.

De las texturas redibujadas se han visto dentro del juego las órdenes «Usar» y «Tirar». Del
resto (resumen «BEFORE STORY», títulos de capítulo, placas de zona, leyenda del mapa y
minimapas) solo se ha comprobado que se leen correctamente de la imagen.

El parche se ha reaplicado al original y reproduce exactamente la candidata publicada.
Las comprobaciones en emulador utilizan PPSSPP 1.20.4, compilación sin ventana, en Linux.

## Limitaciones conocidas

- No hay partida completa ni pruebas en hardware real. Solo se ha jugado el principio del
  juego: tiendas, encargos, mejoras (CUSTOM), ataques EXHAUST, la huida y todo lo posterior a la
  entrada en la primera mazmorra no se han recorrido en pantalla.
- **Nombres de los personajes:** se escriben con el teclado del sistema. En las pruebas solo se
  han introducido en kana (se ven bien); no se ha comprobado si el juego admite letras latinas.
- La fuente es de paso fijo, con letras de 6 píxeles de ancho: es la única forma de que el
  castellano quepa sin modificar el ejecutable. **Tras un nombre de longitud impar insertado
  por el juego** (un enemigo, un objeto) se ve un espacio doble («¡Hierba azul  cae!»), y las
  cifras que inserta el juego salen algo separadas.
- Los nombres de objetos, habilidades y enemigos están limitados por el ancho de sus casillas
  y algunos se abrevian; las descripciones de habilidad se han condensado a 54 letras para que
  quepan en la pantalla de estado. Los topes se han tomado del original y no todos se han visto
  en pantalla.
- Siguen en japonés: los tres rótulos de escena que el juego compone con letras sueltas, las
  diez pantallas de tutorial que son capturas del propio juego, las cartelas caligráficas de
  entrada a cada zona, el aviso legal de arranque, los créditos, los logotipos, el vídeo de
  apertura y los carteles del escenario.
- Un juego de palabras encadenadas (shiritori) entre dos guardias pierde uno de sus enlaces.
- El PPSSPP sin ventana usado para las pruebas se cerró solo tres veces, sin dejar registro y en
  puntos distintos; no se pudo reproducir en ninguno de ellos, ni con el original ni con la
  traducción, y se atribuye al emulador, sin haberlo demostrado. En ese emulador tampoco se
  dibuja el texto de los diálogos de guardado del sistema; guardar y cargar funcionan.

Si encuentras un fallo, indica el lugar, qué estabas haciendo y la versión, y adjunta una
captura o partida guardada propia en una incidencia de GitHub o en la ficha del proyecto.

## Cambios

### v1.0 — 16 de noviembre de 2026

- Primera versión al castellano desde el japonés de PSP.
- Traducción con biblia de términos compartida con la primera parte, revisión editorial
  cruzada de todos los lotes y unificación de nombres y términos.
- Fuente castellana, texturas redibujadas y parche que conserva en su sitio todo lo que no
  se traduce.

## Créditos y aviso legal

Proyecto de **johanderohan**. Traducción, revisión y herramientas asistidas por IA.
La fuente del texto se basa en la tipografía de mapa de bits «misc-fixed 6x13» de X11 (dominio
público). Los rótulos redibujados usan Fira Sans Condensed, Noto Serif y DejaVu Sans Condensed
(licencias libres); no se distribuyen sus archivos de fuente.

Proyecto de aficionados, sin afiliación con los titulares de 7th Dragon ni del juego.
El juego, sus personajes, gráficos, música y marcas pertenecen a sus respectivos titulares.
Este repositorio no contiene la ISO ni herramientas que incluyan el texto del juego.

SHA-256 del parche v1.0: `b1eeeef01ea5b08070837a566826edc7fe9e631fc079c1d514cb3efea2d604e6`.
