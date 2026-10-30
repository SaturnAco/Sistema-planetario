# Sistema solar Sailor (three.js)

Sistema planetario con el Sol, los 8 planetas, Plutón y la Luna de la Tierra. Al hacer clic en un astro se ilumina por los bordes con el color de su Sailor y aparece su retrato abajo a la derecha.

> Autoría: _tu nombre_ · Asignatura: Informática Gráfica

## Vídeo de ejecución
_(Enlazar aquí el vídeo, con tu nombre/autoría visible.)_

## Qué se ha hecho
- **Sistema**: Sol + 9 cuerpos orbitando (escalas y distancias no realistas, para verlos bien), anillo de Saturno y la Luna girando alrededor de la Tierra (grupo hijo del planeta).
- **Iluminación**: el Sol es una `PointLight` (sin atenuación) más una `AmbientLight` tenue; los planetas usan `MeshPhongMaterial`.
- **Texturas**: cada astro busca `src/textures/<id>.jpg` (`sol`, `mercurio`, `venus`, `tierra`, `luna`, `marte`, `jupiter`, `saturno`, `urano`, `neptuno`, `pluton`). Si no existe, se queda con el color de su Sailor.
- **Dos vistas**: general (`OrbitControls`) y subjetiva desde una nave (`FlyControls`). Se alterna con la tecla **V** o el botón.
- **Selección Sailor**: `Raycaster` + halo Fresnel (`ShaderMaterial`, `BackSide`, mezcla aditiva) del color de la Sailor, y panel con retrato (`src/sailors/<id>.png`; si falta, muestra el símbolo astronómico).
- **Interfaz** (`lil-gui` + panel de ayuda): velocidad del tiempo, mostrar/ocultar órbitas, campo de visión y velocidad de la nave.

| Astro | Sailor | Color |
|---|---|---|
| Mercurio | Mercury | azul |
| Venus | Venus | naranja |
| Tierra | Earth* | verde |
| Luna | Moon | amarillo |
| Marte | Mars | rojo |
| Júpiter | Jupiter | verde |
| Saturno | Saturn | violeta |
| Urano | Uranus | celeste |
| Neptuno | Neptune | turquesa |
| Plutón | Pluto | granate |

\*Sailor Earth no es guerrera principal en la serie; se puede cambiar en el array `PLANETAS` de `main.js`.

## Ejecutar
`npm install` y `npm run dev` (o importar el repositorio en CodeSandbox).

## Fuentes
- Prácticas 6 y 7 de la asignatura (código de referencia).
- Documentación de three.js: https://threejs.org/docs/ (Raycaster, OrbitControls, FlyControls, ShaderMaterial).
- Texturas: _indicar origen_ (p. ej. https://www.solarsystemscope.com/textures/ o la fuente de las prácticas).
- Retratos de las Sailors: _indicar origen_ (obra de Naoko Takeuchi; uso educativo).

## Asistencia de IA
Código generado con ayuda de Claude (Anthropic). Conversación: _pegar enlace_.
