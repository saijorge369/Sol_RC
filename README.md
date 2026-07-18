# Sol_RC

Herramienta interactiva para analizar la descarga de un capacitor en un circuito RC.

Autor: Prof. Wong

Incluye:

- tabla editable de datos experimentales;
- calculo de `log10(Vc)`, `ln(Vc)`, `Vc/V0` y `ln(Vc/V0)`;
- comparacion entre cuatro metodos de linealizacion;
- pendiente y constante de tiempo por dos puntos y por ajuste lineal;
- criterio de calificacion para una hoja semilogaritmica base 10 en el eje `y`.
- selector de presentacion: claro, oscuro, noche, Da Vinci y pizarra.
- referencias academicas reales para justificar el modelo fisico y matematico.

Para usarla, abre `index.html` en un navegador moderno.

## Fundamento

Para una descarga RC ideal:

```text
Vc(t) = V0 e^(-t/RC)
tau = RC
ln(Vc) = ln(V0) - t/tau
log10(Vc) = log10(V0) - t/(tau ln 10)
```

Por eso, si la pendiente se obtiene en `log10(Vc)` vs. `t`, entonces:

```text
tau = -1 / (m ln 10) = -0.434294 / m
```

Si se obtiene en `ln(Vc)` o `ln(Vc/V0)` vs. `t`, entonces:

```text
tau = -1 / m
```

## Referencias

- MIT Open Learning Library, 8.02.3x: Introduction to RC and LR Circuits.
- Harvard Natural Sciences Lecture Demonstrations: RC Time Constant.
- Stanford Engineering Everywhere, EE263: Lecture 16 - RC Circuit example.
- OpenStax University Physics Volume 2: 10.5 RC Circuits.
- Khan Academy Electrical Engineering: RC natural response.
- Physics LibreTexts / OpenStax College Physics: DC circuits containing resistors and capacitors.
