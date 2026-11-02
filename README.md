# Mi Progreso / Sport · v2

Tres sesiones de fuerza de cuerpo completo, dos de cardio y dos días de descanso. Registro por serie, agenda reprogramable, medidas opcionales y revisiones en semanas 2, 4, 6, 8 y 12.

## Fuente de verdad y publicación

En el proyecto de trabajo, `v2/` es la única fuente activa; `plan-data.js` contiene rutinas estructuradas y guías generales. `prepare-public.cjs` llama a `build-v2.cjs`: genera `github-public/` y `github-pages/` con lista explícita de archivos, verifica ausencia de referencias personales y genera `plan-general-v2.md` desde el mismo contenido. El repositorio publicado contiene el resultado estático, sin documentos privados. Publicar `main` desde `/(root)` en GitHub Pages. Sin compilación ni backend.

La copia Sites se actualiza desde esos mismos archivos preservando su manifiesto. `seguimiento/integrate-report.cjs` es legado desactivado. Los tar previos son artefactos, no fuentes. La conversión documental inicial no es parte del build público.

## Datos y migración

- `mi-progreso-v2`, esquema 2, ciclos independientes con IDs estables.
- `mi-progreso-v1` permanece intacto. Se archiva completo con nombres originales, medidas, notas y campos desconocidos seguros.
- Cada sesión conserva prescripción, variantes, unidades, máquina y series realizadas.
- Importación validada con previsualización. Incorporar crea ciclos independientes. Reemplazar confirma y guarda primero `mi-progreso-v2-before-import`.
- Los registros permanecen en el navegador. Sin analítica, cuentas o sincronización. Exportar/importar para cambiar de dispositivo u origen.
- Fechas America/Mexico_City. Adherencia excluye fechas futuras y descansos; avance usa 60 sesiones.

## Verificación

En el proyecto: `node --test tests/core.test.cjs`. Pruebas de migración idempotente, campos antiguos, respaldos, errores de almacenamiento, agenda, métricas, dosis, intervalos y medidas. Revisión visual de escritorio y móvil. Sin registros personales de prueba en producción.

## Límites

Propuesta inicial, no certificado médico ni garantía de recomposición. No hay incrementos automáticos por calendario. Peso, cintura y RIR opcionales. Fuentes con alcance y limitaciones. No diagnostica ni estima músculo o grasa.
