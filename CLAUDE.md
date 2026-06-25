# CLAUDE.md — Contexto del proyecto

## Identidad del proyecto

Segundo entregable de la asignatura **Redes I** (semestre 2026-I), E.P. de Ingenieria Informatica y de Sistemas, UNSAAC.
Tema: **Sistema de cableado estructurado del pabellón de la E.P. de Enfermería**.
Es un diseño técnico-académico de infraestructura pasiva (Capa 1 OSI); no incluye configuración lógica, equipos de usuario ni obras civiles pesadas.

## Integrantes

| Apellidos, Nombres | Código |
|---|---|
| Colque Quispe, Fidel Enrique | 231866 |
| Mamani Flores, Natan | 230970 |
| Mayhuire Chacon, Brenda Lucia | 231445 |
| Polo Chura, Marco Rosauro | 141632 |

Docente: Ing. Dueñas Bustinza Dario Francisco.

## Topología y arquitectura de red

- **Topología física:** estrella plana centralizada.
- **MDF único:** Gabinete G09, rack cerrado 42U de 19", ubicado en el Centro de Cómputo (ambiente 208), segundo piso.
- **Sin IDFs ni backbone vertical interno.** Todos los pisos se alimentan directamente desde el MDF con cableado horizontal de cobre.
- **Enlace de campus:** fibra óptica monomodo OS2, 12 hilos, desde DTIC-UNSAAC hasta el ODF del rack.
- **Cableado horizontal:** Cat. 6A U/UTP (10 Gbps / 500 MHz). Ningún enlace supera 90 m.
- **Terminación:** esquema de colores T568-B en ambos extremos.
- **Nomenclatura de puntos (TIA-606-B):** `G09-N[Piso]-[Tipo][Número]` donde Tipo = D (datos) o W (Wi-Fi).

## Distribución de nodos (116 totales)

| Nivel | Función principal | Datos (D) | Wi-Fi (W) | Total |
|---|---|---|---|---|
| 1.o (Administración) | Decanato, Secretarías, Jefaturas, Sala de Lectura | 25 | 3 | 28 |
| 2.o (Cómputo/Aulas) | Centro de Cómputo (24 PCs, aloja el MDF), Laboratorios, Sala Docentes | 42 | 2 | 44 |
| 3.o (Laboratorios/Aulas) | Aulas 301-307, Dir. Calidad 302, Lab. Salud Mat. Infant. 308 | 18 | 2 | 20 |
| 4.o (Auditorio/Aulas) | Of. Administrativa, Centros, Aulas, Lab. Simuladores, Salón Múltiple | 22 | 2 | 24 |
| **Total** | | **107** | **9** | **116** |

## Equipamiento del MDF (Gabinete G09)

- 5 patch panels Cat. 6A de 24 puertos (120 puertos para 116 nodos).
- 6 organizadores horizontales de cable 1U.
- 3 switches de 48 puertos Gigabit PoE+ (IEEE 802.3at) con uplinks SFP+ 10G (144 puertos totales).
- 1 UPS Line-Interactive con AVR 1500 VA / 1000 W, modelo APC SMT1500I (autonomía >= 30 min).
- 1 PDU con supresión de sobretensiones.
- 1 barra de tierra TGB (puesta a tierra <= 5 Ohm, norma TIA-607-B).
- Ventilación forzada con termostato (activa > 35 °C).

## Canalizaciones

- Canaletas PVC con tapa: 40x25, 60x40 y 100x60 mm.
- Bandejas portacables metálicas en cielo raso (soportes cada 1.5 m).
- Ducto EMT en tramos empotrados.
- Cajas de registro.
- Ocupación máxima 40%, separación mínima 150 mm del cableado eléctrico (TIA-569-D).

## Normas y estándares aplicados

| Norma | Uso en el proyecto |
|---|---|
| ANSI/TIA-568-C.0 & C.1 | Topología estrella, distancias, arquitectura general |
| ANSI/TIA-569-D | Canalizaciones, tuberías, rutas de cableado |
| ANSI/TIA-606-B | Etiquetado y administración de infraestructura pasiva |
| ANSI/TIA-607-B | Puesta a tierra de telecomunicaciones |
| ISO/IEC 11801 | Especificaciones de rendimiento complementarias |
| EIA-310-D | Dimensiones del gabinete 19" |

## Presupuesto (referencial, con IGV, en soles)

| Rubro | Monto (S/) |
|---|---|
| Materiales y equipos | 47,209 |
| Mano de obra (30%) | 14,163 |
| Certificación (116 enlaces) | 2,900 |
| **Total** | **64,272** |

Costo por nodo: ~S/ 554. Cable requerido: 5,997 m (20 cajas de 305 m). Longitud promedio por enlace: 47 m (fórmula TIA-568).

## Cronograma

6 semanas de ejecución:
1. Replanteo (2 días, S1)
2. Canaletas y conduit (2 sem, S1-S2)
3. Tendido de cable Cat. 6A (2 sem, S2-S3)
4. Instalación MDF y puesta a tierra (1 sem, S3-S4)
5. Terminación, ponchado y etiquetado (1 sem, S4-S5)
6. Inspección y pruebas preliminares (2 días, S5)
7. Certificación, correcciones y entrega (1 sem, S6)

## Estructura de archivos

```
main.tex                  Documento principal (book, 12pt, a4paper)
Estilo.sty                Carátula UNSAAC y formatos de capítulos especiales
contenido/
  Incluir.tex             Preámbulo: paquetes y declaraciones globales
  cap_1_Memoria_Descriptiva.tex    Cap I: descripción, objetivos, ubicación, alcance, normas
  cap_2_planos.tex                 Cap II: planos por piso, tablas de puntos, rack, backbone, tierra
  cap_3_especificaciones_tecnicas.tex  Cap III: cables, instalación, etiquetado, rack, equipos, certificación
  cap_4_presupuesto.tex            Cap IV: presupuesto general, detallado, metrado, APU, fórmula polinómica
  cap_5_cronograma.tex             Cap V: cronograma de ejecución, compras, Gantt, control
  cap_6_plan_pruebas_certificacion.tex  Cap VI: pruebas, parámetros, reportes, protocolos de aceptación
  cap_7_plan_seguirdad_salud.tex   Cap VII: seguridad eléctrica, EPP, altura, riesgos, emergencias
  anexo.tex                Anexo: matriz de consistencia (plantilla sin llenar)
  introduccion.tex         Vacío
  bibliog.bib              Una sola entrada (Haquehua 2025)
images/
  escudo.png               Escudo UNSAAC para carátula
  imagenes/                Planos de planta (4 pisos), diagramas (backbone, racks, tierra), detalles constructivos
CAMBIOS.md                 Registro de correcciones ya aplicadas
```

## Preámbulo LaTeX (paquetes importados en Incluir.tex)

babel (español), inputenc (utf8), fancyhdr, graphicx, geometry (2.54 cm), newtxtext + newtxmath, amsmath, ragged2e, amsthm, etoolbox, chngcntr, setspace, multirow, amssymb, tikz, hyperref (breaklinks), caption, amsfonts, natbib, float, titlesec, titletoc, fontenc (T1), enumitem, array, pdflscape, subcaption, longtable, tocloft.

Comando utilitario: `\figpend{descripción}` genera un placeholder para figuras pendientes.

## Estilo de redacción

- Español técnico-académico formal, tercera persona impersonal.
- Vocabulario preciso de telecomunicaciones (TIA/ISO).
- Capítulos en mayúsculas y romanos (`CAPÍTULO I`, `CAPÍTULO II`...).
- Secciones con numeración arábiga (1.1, 1.2...).
- Tablas con caption arriba (`\caption` antes de `\begin{tabular}`), figuras con caption abajo.
- Listas con `\begin{itemize}[label=$\bullet$,leftmargin=1.4em]`.
- Unidades con `\,` como separador fino (10\,Gbps, 500\,MHz, 90\,m).
- Abreviaciones recurrentes: MDF, IDF, TGB, TMGB, TBB, ODF, PDU, UPS, PoE+, AP, DTIC.
- Sin emojis. Sin primera persona.

## Decisiones de diseño ya tomadas

- Se eliminó toda referencia a CCTV/videovigilancia (ver CAMBIOS.md).
- Se unificaron todas las cifras a 116 nodos en todos los capítulos.
- Se migró la nomenclatura de puntos al formato `G09-N[Piso]-[Tipo][Número]`.
- Se recalculó el presupuesto completo con las cifras actualizadas.
- No hay backbone vertical interno: todo es cableado horizontal directo al MDF.
- Categoría de cable: 6A (no 6).
- Puesta a tierra: <= 5 Ohm.
- UPS corregida de "online doble conversión 1350 W" a line-interactive AVR 1000 W (modelo real SMT1500I).
- AP Aruba AP25: tasa corregida de 2.97 Gbps a 5.3 Gbps agregado; specs completadas (puerto 2.5 GbE, WPA3).
- Se agregaron 107 cajas de pared PVC (S/ 535) como ítem en presupuesto y subsección en cap_3.
- Desglose explícito de jacks (125), faceplates (107), cajas de pared (107) y cajas de paso (9) en sección faceplate.
- Aclaración en cap_4: el APU (S/ 228.07/punto) no se multiplica para obtener el total de obra.
- Presupuesto recalculado en cadena: materiales 47,209 / mano de obra 14,163 / total 64,272 / nodo ~554.
- PDU formalizada como componente: tabla de specs en §3.6.1 (cap3), ítem en presupuesto detallado (cap4), S/ 280.
- Los 3 switches operan activos desde el inicio (96 puertos de 2 switches serían insuficientes para 116 nodos).
- TGB ubicada físicamente en el interior del gabinete (montaje 0U en lateral).
- Patch panel corregido de "Descargado" (modular, requiere jacks extra) a "Cargado/Fijo" (puertos integrados de fábrica). Coherente con el metrado de 125 jacks (solo lado usuario + repuesto). Sin impacto en presupuesto.

## Advertencias para ediciones futuras

- Al modificar cantidades de nodos, verificar consistencia en: cap_2 (tablas por piso + resumen), cap_3 (patch panels, switches, certificación, cajas de pared), cap_4 (presupuesto, metrado, cronograma de compras, APU), cap_6 (certificación).
- El APU (Tabla 28) se dejó en S/ 228.07 sin incluir la caja de pared; no modificarlo salvo decisión explícita.
- Las imágenes son archivos estáticos; si se cambian datos en tablas, las figuras de los planos no se actualizan automáticamente.
- El archivo `cap_7_plan_seguirdad_salud.tex` tiene una errata intencional en el nombre ("seguirdad" en lugar de "seguridad"); no renombrar sin actualizar `main.tex`.
- La matriz de consistencia del anexo está vacía (plantilla genérica).
- La bibliografía solo tiene una entrada; agregar referencias según sea necesario.
 