# DnD Dices

Calculadora de dados y asistente de tiradas para partidas de rol estilo Dungeons & Dragons. Este proyecto ofrece una interfaz visual para hacer tiradas de dados, calcular modificadores de atributos, habilidades y salvaciones, manejar contadores personalizados y enriquecer partidas con tiradas de ataque y críticos.

## Características principales

- Calculadora de dados con expresiones tipo `2d6 + 3` y operaciones básicas.
- Tiradas de atributos (FUE, DES, CON, INT, SAB, CAR) con opción de competencia.
- Manejo de habilidades y salvaciones con competencia, doble competencia y "Jack of all trades".
- Tiradas personalizadas de ataque con opción de crítico.
- Secciones plegables para simplificar la interfaz.
- Contadores personalizables con nombres y valores, persistentes en `localStorage`.
- Persistencia local de modificadores y contadores para mantener datos entre recargas.

## Estructura del proyecto

- `index.html` - Interfaz principal del proyecto con todas las secciones visibles.
- `app.js` - Lógica principal para el cálculo de tiradas, habilidades, salvaciones y resultados críticos.
- `counters.js` - Control de los contadores personalizables y almacenamiento en `localStorage`.
- `separators.js` - Comportamiento de colapsado/expandido de secciones y bloqueo de edición.
- `index.scss` - Estilos base y definiciones de tipografía.
- `src/index.css` - Posible hoja de estilos de salida procesada para el proyecto.
- `assets/` - Archivos generados de estilo y script utilizados en la versión distribuida.
- `dist/` - Carpeta de distribución con salida compilada.

## Uso local

1. Clona el repositorio o descarga los archivos.
2. Abre `index.html` en tu navegador.
3. Usa el panel principal para:
   - Ingresar expresiones de dados y presionar `=`.
   - Seleccionar atributos, habilidades y salvaciones.
   - Activar competencia, doble competencia o "Jack of all trades".
   - Añadir y controlar contadores personalizados.
   - Ingresar tiradas de ataque personalizadas con casillas de crítico.

> Nota: los valores de modificadores y contadores se guardan localmente en el navegador.

## Detalles de implementación

- `app.js` usa `Math.random()` para simular tiradas de dados.
- El resultado de `d20` se colorea en rojo para 1 y en verde para 20.
- Las expresiones de dados se evalúan con un parser simple basado en `eval()` tras reemplazar `NdM` por sumas individuales.
- Las secciones del panel pueden plegarse con los controles de las pestañas y bloquearse para evitar edición accidental.

## Recomendaciones

- Usar un navegador moderno para asegurar compatibilidad con `localStorage` y las API estándar.
- Si se desea, limpiar el código eliminando los archivos de distribución (`assets/`, `dist/`) y centralizar la fuente en la versión original.

## Licencia

Este repositorio no incluye una licencia explícita. Si deseas, puedes añadir una licencia como `MIT`, `GPL` u otra según tus necesidades.
