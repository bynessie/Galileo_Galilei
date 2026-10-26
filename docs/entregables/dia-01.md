---
kaizen_dojo: "2026"
formato: "Entregable diario"
evidencia: "E1"
dia: 1
responsable_registro: "ChocoTeam"
estado: "Completo"
fecha: "2026-10-26"
revision_docente: "PENDIENTE"
---

# E1 · Día 1 — ATREVERSE | Contrato de misión, inventario y dōjō


## 0 · Identificación, equipo y logística del dōjō

| Campo obligatorio | Dato |
|---|---|
| Fecha y horario de esta sesión | 2026-10-26; 09:00–11:00 (horario reservado indicado por el equipo) |
| Nombre / alias del equipo | ChocoTeam |
| Misión / plataforma | M01 mini-sumo autónomo (robot Galilei) |
| Objetivo verificable del robot (una frase) | Optimizar los procesos de un minisumo y realizar un robot 100% competitivo.|
| **Dōjō asignado — campus, edificio y sala/taller exactos** | **Laboratorio de electrónica de CTA** |
| Puesto o zona dentro del dōjō | Dohyō |
| Horario / reserva confirmada | 09:00–11:00 del 2026-10-26; autorizó: Camilo Rene Duque |
| Responsable del espacio y contacto institucional | Camilo Rene Duque, Director de Mecatrónica. Canal institucional: camilo.duque@tec.mx |
| Acceso, aforo y ajustes de accesibilidad | Sin restricciones de acceso o aforo; sin ajustes de accesibilidad necesarios |
| Salidas, botiquín, extintor y punto de reunión | Validar si existe |
| Zonas segregadas por riesgo | N/A |
| Ubicación de materiales y resguardo nocturno | Locker de Artemis. Responsables: Marian Zamarripa, Juan Carlos Muñoz y Fátima Romero |
| Plan de sustitución si falla el espacio | Pedir prestado al equipo de robótica|
| Instructor o supervisor presente en la sesión | Camilo Rene Duque |

> ⛔ **No se permite avanzar a pruebas físicas sin dōjō concreto y autorización del responsable.** No inventar salón, número de laboratorio ni recursos que no hayan sido confirmados.

## 1 · Integrantes, responsabilidades, accesibilidad y decisiones (0–15 min)

| Alias GitHub | Rol inicial | Carta y frontera (D/S/E; F1–F4) | Alcances ID (1–3) | Kit personal (archivo) | Necesidad de apoyo o accesibilidad acordada |
|---|---|---|---|---|---|
| @a00574470-hash (Jonathan Escamilla) | Programador | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | `participantes/a00574470-hash/compromiso.md` (subida: PENDIENTE A AGREGAR) | PENDIENTE A AGREGAR |
| @carlangas1291 (Carlos Muñoz) | Manufactura | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | `participantes/carlangas1291/compromiso.md` (subida: PENDIENTE A AGREGAR) | PENDIENTE A AGREGAR |
| @choco (Fátima Romero) | Diseñadora CAD | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | `participantes/choco/compromiso.md` (subida: PENDIENTE A AGREGAR) | PENDIENTE A AGREGAR |
| @bynessie (Marian Zamarripa) | Manufactura y logística | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | `participantes/bynessie/compromiso.md` (subida: PENDIENTE A AGREGAR) | PENDIENTE A AGREGAR |

**Acuerdo de colaboración:** PENDIENTE A AGREGAR (cómo se toman decisiones, cómo se resuelven conflictos, apoyos senpai–kōhai, pausas y distribución equitativa de participación).

## 2 · Demostración de la plataforma y seguridad (15–35 min)

| Elemento | Observación directa | Evidencia / vínculo |
|---|---|---|
| Plataforma base inspeccionada (estado, modelo, ID inventario) | Robot MOCHI (mini-sumo). Estado: diseñado. ID de inventario: PENDIENTE A AGREGAR | `BOM_MOCHI.pdf` (ruta en repositorio: PENDIENTE A AGREGAR); fotos: PENDIENTE A AGREGAR |
| Funciones existentes y límites comprobados | Límites considerados: limitantes de la maquinaria y falta de tiempo para un desempeño máximo | PENDIENTE A AGREGAR |
| Paro de emergencia / desconexión segura ensayados | **No ensayados** | — |
| Restricciones de competición o exhibición verificadas | Reglamento de referencia: Robolympics. Verificación puntual de reglas: PENDIENTE A AGREGAR | Fuente: reglamento Robolympics (enlace: PENDIENTE A AGREGAR) |
| Riesgos vistos y medidas activas | PENDIENTE A AGREGAR | `docs/seguridad.md` (PENDIENTE A AGREGAR) |

**Normas específicas según misión (M01):** protecciones de alimentación; desarmar motores antes de tocar ruedas; dohyō delimitado, rival de referencia y bordes seguros.

## 3 · Diagnóstico práctico colectivo (35–65 min)

**Condición inicial V0 de la plataforma:** Robot MOCHI en estado de diseño. Existen BOM, firmware principal y guía de código (ver capacidades documentadas abajo). Qué funciona y qué falta en físico: PENDIENTE A AGREGAR.

| Prueba diagnóstica | Condición y procedimiento | Resultado observado / unidad | Problema / causa probable | Evidencia |
|---|---|---|---|---|
| 1: movimiento o comunicación | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| 2: lectura de sensor | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| 3: comportamiento de la misión | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |

*No se registran pruebas realizadas en esta sesión.*

**Capacidades ya disponibles y dependencias:**

Capacidades **documentadas en los archivos del equipo** (`main-code.md`, `code-guide.md`); no se han verificado en esta sesión:

- Controlador: PCB XMotion V3 (JSUMO), Arduino Leonardo, librería `xmotionV3.h`.
- Sensado: 4 sensores IR digitales de oponente (externo izq. pin 0, frontal izq. pin 1, frontal der. pin 2, externo der. pin 4), 2 sensores QTR analógicos de línea (izq. A5, der. A4) y módulo starter (A0).
- Lógica en el firmware: arranque por starter; evasión del borde con los QTR; ataque según qué sensores IR detectan al oponente; modo búsqueda (paro y giro) si no hay oponente.
- Calibración de motores por porcentaje (`calib_left = 170`, `calib_right = 255`).
- Estrategia activada según `code-guide.md`: **#2** (velocidad media hasta detectar oponente y luego cambio de potencia para aprovechar inercia y fricción).

Dependencias entre integrantes: PENDIENTE A AGREGAR.

## 4 · Integración de Mission Forge C2 y pacto de alcances (65–100 min)

Cada participante debe colocar el archivo **Markdown original generado por la web** en:

`participantes/<alias>/compromiso.md`

Se conserva íntegro (incluido el frontmatter y la lista de katas). Los nuevos alcances/katas diseñados por el participante quedan claramente marcados como *propuesta propia* y requieren aprobación técnica.

**Catálogo de referencia:** [Google Sheets C2](https://docs.google.com/spreadsheets/d/1FKxFzoyu9KJb3RlOwB609vliS5hAtmwWFu2G2zG3Ky4/edit) · **Configurador Mission Forge:** [`herramientas/mission-forge-c2.html`](../../herramientas/mission-forge-c2.html) (descárgalo y ábrelo en el navegador; funciona sin Internet).

| Alias | Kit enlazado | Alcance principal | Complementos | Katas elegidos o nuevos | Horas mín.–máx. | Evidencia final esperada | Negociación aprobada |
|---|---|---|---|---|---|---|---|
| @a00574470-hash | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| @carlangas1291 | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| @choco | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| @bynessie | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |

**Resultado de negociación grupal:** PENDIENTE A AGREGAR (puntos de integración; interfaces entre códigos/firmware/sensores/estructura; prioridad si no hay tiempo).

## 5 · Inventario exhaustivo y especificación de materiales (obligatorio)

### 5.1 Inventario maestro del equipo

Fuente de las filas MAT-002 a MAT-012: `BOM_MOCHI.pdf` (tipo de cambio $17.52 MXN; total del BOM $3,132.02 MXN). Las columnas de cantidad confirmada, ubicación por ítem, responsable por ítem, estado, alternativa y día requerido quedan pendientes porque el equipo aún no las ha confirmado. Ubicación general de materiales: locker de Artemis.

| ID | Categoría | Material o recurso (especificación exacta) | Cantidad requerida + unidad | Cantidad confirmada | Fuente/proveedor o dueño | Ubicación física o ruta digital | Responsable | Estado (disponible/reservado/falta) | Alternativa compatible | Día requerido |
|---|---|---|---|---|---|---|---|---|---|---|
| MAT-001 | Robot/plataforma | Robot MOCHI, mini-sumo autónomo (diseño; referencia visual en el BOM) | 1 ud. | PENDIENTE A AGREGAR | Equipo | Locker de Artemis (confirmación PENDIENTE A AGREGAR) | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-002 | Sensor | JS04F Digital distance sensor (JSUMO): detecta objetos desde 40 cm, 3.3–5 V (15 mA), cable 15 cm, 12.5 × 17.7 × 11.5 mm. $219.00 c/u | 4 ud. | PENDIENTE A AGREGAR | JSUMO | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-003 | Actuador | Core DC Motor JS16661 (JSUMO): 6 V (120 mA), 750 RPM, hasta 15 V. $280.32 c/u | 2 ud. | PENDIENTE A AGREGAR | JSUMO | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-004 | Sensor | QTR-1RC Infrared Sensor, paquete de 2 piezas (JSUMO): 5 V, 20–25 mA, 7.62 × 12.7 × 2.54 mm. $84.10 | 1 paquete (2 pzas) | PENDIENTE A AGREGAR | JSUMO | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-005 | Electrónica | Batería LiPo R-LINE (TATTU): 3S, 11.1 V, 95 C, 21 × 18.5 × 63 mm. $303.00 | 1 ud. | PENDIENTE A AGREGAR | AliExpress | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-006 | Electrónica | PCB XMotion V3 (JSUMO), controlador, 80 × 30 × 7 mm. $787.52 | 1 ud. | PENDIENTE A AGREGAR | JSUMO | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-007 | Mecánica | JS2622S Steel-Silicone Wheel Pair (JSUMO): orificio 3 mm, diámetro 26.5 mm, grosor 22 mm. $254.04 | 1 par | PENDIENTE A AGREGAR | JSUMO | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-008 | Mecánica | Mini Katana Blade (JSUMO), cinta de 3 mm, 22 × 100 × 0.25 mm. $86.72 | 1 ud. | PENDIENTE A AGREGAR | JSUMO | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-009 | Mecánica | Placa de latón para peso, 1/4", 50 × 93 mm. $0.00 | 1 ud. | PENDIENTE A AGREGAR | La paloma | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-010 | Mecánica | Fleje de acero al carbono, grosor 1.18 mm, 99 × 45.3 mm (aprox.). $90.00 c/u | 2 ud. | PENDIENTE A AGREGAR | Digital | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-011 | Tornillería | Tornillo M3 con cabeza avellanada (fijación del fleje). $0.00 | 2 ud. | PENDIENTE A AGREGAR | El tornillo | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-012 | Tornillería | Tornillo M3 con cabeza hueca hexagonal (fijación de motores). $0.00 | 4 ud. | PENDIENTE A AGREGAR | El tornillo | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-013 | Sensor/arranque | Módulo starter (mencionado en `main-code.md`; no aparece en el BOM). Modelo: PENDIENTE A AGREGAR | 1 ud. | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-014 | Software/datos | Arduino IDE (versión: PENDIENTE A AGREGAR) con librería `xmotionV3.h`; firmware en `main-code.md` | — | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| MAT-015 | Zona de pruebas | Dohyō en el laboratorio de electrónica de CTA (dimensiones y rival de referencia: PENDIENTE A AGREGAR) | 1 ud. | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | Laboratorio de electrónica de CTA | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |

También disponible el archivo [`datos/inventario_materiales.csv`](../../datos/inventario_materiales.csv) para registrar muchos materiales sin agrandar esta tabla.

### 5.2 Lista de cotejo específica por plataforma (M01 · Mini-sumo autónomo)

| Elemento de la lista M01 | Estado según los archivos entregados |
|---|---|
| Chasis y material para cuñas | Placa de latón (MAT-009), fleje de acero (MAT-010) y Mini Katana Blade (MAT-008). Chasis completo: PENDIENTE A AGREGAR |
| Ruedas/motores/soportes | Ruedas MAT-007, motores MAT-003, tornillería MAT-011 y MAT-012. Soportes: PENDIENTE A AGREGAR |
| Driver, controlador y firmware | PCB XMotion V3 (MAT-006) y firmware en `main-code.md` |
| Batería/cargador/fusible | Batería MAT-005. Cargador y fusible: PENDIENTE A AGREGAR |
| Sensores de borde y rival | QTR (MAT-004) y JS04F (MAT-002) |
| Cableado/conectores | PENDIENTE A AGREGAR |
| Dohyō/rival de referencia | Dohyō: ver MAT-015. Rival de referencia: PENDIENTE A AGREGAR |
| CAD/impresora 3D/herramientas | PENDIENTE A AGREGAR |
| Instrumentos de medición y protocolo de paro | PENDIENTE A AGREGAR |

**Enlaces a fichas técnicas / instrucciones de conexión, fabricación y seguridad:** URLs de productos incluidas en `BOM_MOCHI.pdf` (JSUMO y AliExpress); `code-guide.md` para el código. `XMotion-V3.md` está en el repositorio sin contenido; ficha de la PCB: PENDIENTE A AGREGAR.

### 5.3 Riesgos de recursos y abastecimiento

| Bloqueante | A qué alcance afecta | Solución prevista / fecha y responsable | Impacto si no se resuelve |
|---|---|---|---|
| Bloqueantes confirmados por el equipo: PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| Por verificar: la batería documentada en `main-code.md` es LiPo 2S 800 mAh y el BOM lista una LiPo 3S 11.1 V 95 C (TATTU) | Alimentación | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |
| Por verificar: cargador, fusible, cableado/conectores y módulo starter no aparecen en el BOM | Alimentación y arranque | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |

**Materiales completos para ejecutar el Día 2:** PENDIENTE A AGREGAR (Sí / Parcial / No). **Confirmado por:** PENDIENTE A AGREGAR.

## 6 · Kata 0 — exploración técnica de arranque (100–160 min)

| Integrante/alcance | Pregunta técnica | Mini-prueba o prototipo de exploración | Resultado o error observado | Evidencia enlazada | Acción necesaria antes de D2 |
|---|---|---|---|---|---|
| PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR | PENDIENTE A AGREGAR |

**Integración entre subequipos:** PENDIENTE A AGREGAR.

## 7 · Cierre: contrato técnico y puerta de salida E1 (160–180 min)

- [ ] El objetivo colectivo tiene condición de éxito verificable.
- [ ] Cada estudiante depositó **su kit Markdown original** en `participantes/<alias>/compromiso.md`.
- [ ] Cada estudiante completó [E1 personal](../../participantes/_plantilla/dias/E1.md) y definió frontera, evidencia y alcance negociado.
- [ ] El inventario está **completo** y cada recurso indica cantidad, especificación, disponibilidad y responsable.
- [ ] Se asignó **dōjō específico** con edificio, salón/taller, horarios, supervisión y autorización.
- [ ] Se inspeccionaron riesgos, paro y condiciones de seguridad de la plataforma.
- [ ] Se identificaron dependencias y bloqueos del Día 2; están bajo control o se ajustó la misión.
- [ ] El profesor aprobó el alcance y la seguridad, o registró observaciones y una alternativa viable.

*(Casillas sin marcar: PENDIENTE A AGREGAR la confirmación de cada una.)*

**Estado del gate:** PENDIENTE A AGREGAR (APROBADO / APROBADO CON CONDICIONES / REPLANIFICAR).

**Condiciones, responsables, fecha y próxima decisión:** PENDIENTE A AGREGAR.

**Revisor docente:** PENDIENTE A AGREGAR · **Enlace a commit/PR:** PENDIENTE A AGREGAR

**Criterio mínimo E1:** existe un contrato de misión y frontera individual, hay evidencia del punto de partida, un inventario verificable y un espacio de trabajo autorizado. La ausencia de algún material crítico NO debe esconderse.
