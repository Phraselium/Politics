# Rúbricas de evaluación

Versión 1.0 — fijada el 2026-10-12. **No se modifica durante el análisis.** Cualquier cambio exige nueva versión, nota en `/salida/changelog.md` y reevaluación completa.

## 1. Tipología de contenidos del programa (Fase 2)

| Tipo | Definición | Ejemplo de forma |
|---|---|---|
| MEDIDA | Acción concreta con instrumento identificable (norma, impuesto, partida, organismo, prestación) | "Deflactaremos la tarifa del IRPF…" |
| OBJETIVO | Meta, normalmente cuantificada o fechada, sin instrumento | "Reduciremos el paro al 8 % en 2030" |
| DECLARACION | Enunciado genérico sin meta ni instrumento | "Apostamos por una sanidad de calidad" |

Solo las MEDIDAS se puntúan en viabilidad. OBJETIVOS y DECLARACIONES se cuentan para el **grado de concreción** = MEDIDAS / total de unidades extraídas.

`estatus_actual`: `ya en vigor` | `en tramitación` | `nueva` | `deroga algo vigente`. Una medida marcada `ya en vigor` se señala como **promesa de algo ya aprobado** y no suma al grado de concreción.

## 2. Veredictos de verificación (Fase 4A)

| Veredicto | Criterio |
|---|---|
| VERIFICADO | Coincide con la fuente oficial (tolerancia: redondeo a la cifra significativa que usa el programa) |
| ENGAÑOSO | Dato cierto, pero periodo, base, unidad o comparación elegidos de modo que distorsiona la conclusión que sugiere el texto |
| FALSO | Contradicho por fuente oficial publicada **antes** de la fecha del programa |
| INVERIFICABLE | No existe fuente oficial que permita contrastarlo, o el enunciado es demasiado vago |

Se usa "falso", nunca "mentira": no se atribuye intención. En la revisión adversarial (4B) un veredicto ENGAÑOSO o FALSO se rebaja un nivel si existe una lectura favorable razonable **con fuente**; se documentan ambos argumentos.

## 3. Viabilidad (Fase 4C) — escala 1–5 por eje

### 3.1 Presupuestaria (PIB de referencia en `parametros.yaml`)
| Puntos | Criterio |
|---|---|
| 5 | Coste < 0,1 % PIB, o financiación concreta y creíble |
| 4 | 0,1–0,5 % PIB con financiación parcialmente detallada |
| 3 | 0,5–1 % PIB, o financiación genérica ("lucha contra el fraude", "crecimiento") |
| 2 | > 1 % PIB sin financiación, o incompatible con la senda de gasto neto UE |
| 1 | Coste no estimable, o contradicho por AIReF / Comisión Europea |

Si el partido no da coste: estimación propia con rango (bajo / central / alto), método explícito y etiqueta `estimación propia`. Coste **estático** y efectos **dinámicos** se registran por separado; los dinámicos solo se aceptan con evidencia empírica citada. La puntuación usa el coste central estático.

### 3.2 Jurídica
| Puntos | Criterio |
|---|---|
| 5 | Basta real decreto o reglamento (incluye RDL convalidable) |
| 4 | Ley ordinaria |
| 3 | Ley orgánica (mayoría absoluta del Congreso, art. 81 CE) |
| 2 | Choca con derecho UE o requiere negociación en Bruselas |
| 1 | Requiere reforma constitucional (art. 167 o 168 CE) |

Si concurren varios requisitos se toma el más exigente.

### 3.3 Competencial
| Puntos | Criterio |
|---|---|
| 5 | Competencia estatal exclusiva (art. 149 CE) |
| 3 | Compartida o requiere acuerdo con CCAA (bases estatales + desarrollo autonómico, CPFF, conferencias sectoriales) |
| 1 | Competencia autonómica, local o de la UE |

### 3.4 Parlamentaria (media de encuestas de `parametros.yaml`)
| Puntos | Criterio |
|---|---|
| 5 | Mayoría requerida alcanzable por el bloque que la propone |
| 3 | Necesita socios cuyo programa no la rechaza |
| 1 | Necesita socios cuyo programa la contradice expresamente |

Mayorías de referencia: simple (votación en Congreso), absoluta 176 (ley orgánica, investidura 1.ª votación), 3/5 = 210 (reforma art. 167; nombramientos CGPJ/TC), 2/3 = 234 (art. 168). El Senado se considera cuando su mayoría pueda retrasar o vetar (art. 90 CE) o sea necesaria (art. 167/168).

Para partidos **territoriales** este eje se reinterpreta: capacidad de arrancar la medida en una negociación de investidura o presupuestos, según la aritmética de la media de encuestas (¿son sus escaños necesarios para alguna mayoría plausible?).

### 3.5 Temporal
| Puntos | Criterio |
|---|---|
| 5 | Ejecutable en el primer año |
| 3 | Ejecutable dentro de la legislatura |
| 1 | Horizonte superior a 4 años |

(2 y 4 se usan para casos intermedios con justificación.)

## 4. Reglas generales
- Toda puntuación lleva justificación y fuente.
- Si falta un dato: "no disponible"; nunca se imputa.
- Mismo número de medidas (15) y mismo nivel de detalle por partido; las desviaciones se explican en la Fase 5.
