# CAMBIOS.md — Registro de correcciones aplicadas

## Problema 0 — Eliminación de CCTV
- cap_1 (1.1): eliminada mención a "cámaras de video vigilancia (CCTV)" en descripción general.
- cap_1 (1.2.2): eliminada referencia a "cámaras de seguridad" en objetivos específicos.
- cap_1 (1.4): eliminado el bullet completo "Infraestructura para Video Vigilancia (CCTV)".
- cap_2 (Tabla 8): eliminada la columna CCTV (C).
- cap_3 (3.1.1): eliminada mención a "cámaras de seguridad" en cableado horizontal.
- cap_3 (3.4.2): eliminada referencia a "las 8 cámaras de seguridad" en switches PoE+.
- cap_3 (3.5.1): eliminada mención a "sistema de video vigilancia" en UPS.
- cap_4 (Tabla 10, ítem 5): "Caja de paso/registro (techo APs y CCTV)" → "(APs)"; cantidad 17 → 9.
- cap_4 (metrado texto): eliminada referencia a "8 de CCTV" en cajas de paso.
- cap_6 (6.4): eliminada referencia a "cámaras" en protocolos de aceptación PoE.
- cap_7 (7.2): "Access Points, cámaras, canaletas" → "Access Points, canaletas".
- cap_7 (Tabla 19): "Instalación de AP y cámaras" → "Instalación de AP en techos".

## Problema 1 — Total de nodos = 116, patch panels = 5
- cap_2 (2.3): 62 → 116 nodos, 3 → 5 patch panels, 72 → 120 puertos.
- cap_3 (3.4.1): 3 → 5 patch panels, 62 → 116 nodos.
- cap_3 (3.4.2): 2 → 3 switches, 96 → 144 puertos, 62 → 116 nodos.
- cap_3 (3.6): 62 → 116 puntos de red en certificación.
- cap_4: todos los 62 → 116 en intro, tablas y textos.

## Problema 2 — Tablas 4–8 reescritas con distribución real
- Tabla 4 (Piso 1): 28 puntos (25D + 3W), columnas [N.º, Ambiente, Puntos, Tipo, Uso].
- Tabla 5 (Piso 2): 44 puntos (42D + 2W), mismas columnas.
- Tabla 6 (Piso 3): 20 puntos (18D + 2W), códigos G09-N3-Dxx / G09-N3-Wxx.
- Tabla 7 (Piso 4): 24 puntos (22D + 2W), códigos G09-N4-Dxx / G09-N4-Wxx.
- Tabla 8 (Resumen): 107D + 9W = 116 total, sin columna CCTV.
- Textos intro 2.2.1–2.2.4 actualizados con nuevas cantidades.
- Captions de figuras pisos 3 y 4 actualizados.

## Problema 3 — Presupuesto, metrado y APU recalculados
- Tabla 9: total S/ 47,222 (materiales 34,094 + M.O. 10,228 + cert. 2,900).
- Tabla 10: 14 partidas recalculadas; subtotal materiales = S/ 34,094.
- Tabla 11: 116 × 35 m = 4,060 m + 10 % = 4,466 m → 15 cajas.
- Tabla 12 (APU): cable a S/ 3.19/m → S/ 111.65; costo por punto = S/ 191.15.
- Costo/nodo: 47,222 / 116 ≈ S/ 407.
- Tabla 14 (compras): reajustada a S/ 36,994 (materiales 34,094 + cert. 2,900).

## Problema 4 — Nomenclatura unificada G09-N[Piso]-[Tipo][Número]
- Tablas 6 y 7: códigos reescritos (G09-D14…D33 → G09-N3-D68…, G09-N4-D86…).
- Tabla 17 (cap_6): ejemplo G09-N2-D01 → G09-N2-D26 (numeración global).
- Cap_3 (3.2.3): el formato ya estaba definido correctamente, sin cambios.

## Problema 5 — Cat. 6 → Cat. 6A
- cap_2 (2.2.3): "outlet doble Cat.6" → "salida Cat. 6A" (reescritura del intro).
- La mención comparativa en cap_3 ("Categoría 6" como referencia al estándar anterior) se mantiene.

## Problema 6 — Puesta a tierra ≤ 5 Ω
- Ya estaba correctamente indicado en cap_3 (3.5.2) y cap_6 (6.4). Sin cambios necesarios.

## Definición de punto de red
- Añadida en cap_2 (inicio de sección 2.2): "Cada punto de red equivale a un enlace permanente…"

## Notas
- Todas las cifras cuadran de extremo a extremo.
- Las imágenes no fueron modificadas; las figuras cuyos captions contenían cifras fueron actualizados.
- La fórmula polinómica (cap_4) mantiene coeficientes aproximados originales (a ≈ 0.45, b ≈ 0.35, c ≈ 0.20), suficientes para un proyecto académico según el propio texto.
