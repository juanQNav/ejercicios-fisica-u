# Objective: Add the requested Sears & Zemansky Chapters 6–7 exercises and session-scoped study aids to `index.html`.
# Branch: `feat/chapter-6-7-energy-exercises` | Delivery strategy: `ask-on-risk` | Chain strategy: `stacked-to-main` | Authored-line forecast: >400 (initial estimate ≈900 additions) | Test runner: no dedicated runner found; validate inline JavaScript and rendered data.

## Specs

### S1 — Requested exercise set
User request: "los problemas nuevos son  6.10, 12, 14, 15, 16, 17, 19, 20, 21, 23, 25, 27.43, 44, 45, 46, 47,48, 49, 73, 76, 81, 82\n 7.39, 42, 43, 46, 47, 49, 50, 55, 56, 63, 65, 66, 68, 70, 74, 75."
Acceptance: Add exactly the requested exercise IDs under Chapters 6 and 7, using the specified textbook and solution-manual sources. Check there are no duplicate IDs and all requested IDs are present.
Checks: JavaScript syntax validation; exercise-ID inventory.

### S2 — Exercise presentation
User request: "tienes que hacerlos en el index.html como los otros que se han hecho."
Acceptance: Follow the existing exercise-card data/rendering structure in `index.html`.
Checks: Structural readback; browser-render smoke check if the available runtime supports it.

### S3 — Required learning content
User request: "recuerda hay que hacer problma, el diagrama, video sugerido, consejo/tip, solucion paso a paso, y respuesta"
Acceptance: Each new exercise includes a problem statement, rendered diagram, suggested video, tip, step-by-step solution and final answer.
Checks: Exercise data-field completeness; every diagram key resolves to a real SVG generator.

### S4 — Study aids limited to this session's exercises
User request: "sería bueno complementar las mnemotecnias, flashcards y formulario con respecto y unicamente a los problemas que resolviste en esta sesión."
Acceptance: Add only formulas, mnemonics and flashcards relevant to the requested Chapters 6–7 problems; do not expand unrelated chapter aids.
Checks: Read back the new chapter-specific study-aid entries and confirm their formula coverage is exercised by the added problems.

## Tasks
- T1 — S1–S3: Add Chapter 6 exercises 6.10–6.27 with solutions, diagrams, video suggestions and tips; route: inline; status: complete (12 requested IDs, SVG mappings, Node syntax and ID checks passed); commit: pending.
- T2 — S1–S3: Add remaining requested Chapter 6 exercises 6.43–6.82; route: inline; status: pending; commit: pending.
- T3 — S1–S3: Add requested Chapter 7 exercises 7.39–7.56; route: inline; status: pending; commit: pending.
- T4 — S1–S3: Add requested Chapter 7 exercises 7.63–7.75; route: inline; status: pending; commit: pending.
- T5 — S4: Add session-scoped Chapter 6–7 formula reference, flashcards and mnemonics; route: inline; status: pending; commit: pending.
- T6 — S1–S4: Validate all requested IDs, exercise fields, diagram mappings, inline JavaScript syntax and rendered page structure; route: inline; status: pending; commit: pending.

## Log

### L1 — Original request (verbatim)
@index.html

en notebooklm hay una notebook llamada "Física Universitaría".

de ahí vas a tomar la fuente "204-307_Fisica-Universitaria-Sears-Zemansky-12ava-Edicion-Vol1.pdf", Para encontrar los ejercicios.

y usaras la fuente "solucionario-fisica-u-sears-zemansky.pdf" para solucionar los problemas.

tambien hay una notebook llamada "Videos FISICA", esta la usaras para los videos recomendasos

los problemas nuevos son  6.10, 12, 14, 15, 16, 17, 19, 20, 21, 23, 25, 27.43, 44, 45, 46, 47,48, 49, 73, 76, 81, 82
 7.39, 42, 43, 46, 47, 49, 50, 55, 56, 63, 65, 66, 68, 70, 74, 75.

tienes que hacerlos en el index.html como los otros que se han hecho.

recuerda hay que hacer problma, el diagrama, video sugerido, consejo/tip, solucion paso a paso, y respuesta

sería bueno complementar las mnemotecnias, flashcards y formulario con respecto y unicamente a los problemas que resolviste en esta sesión.

### L2 — Exploration and forecast
No `package.json` or JavaScript test files are present. The 39 source-backed exercise cards, their SVG diagrams and the requested study aids are forecast to exceed the 400-line review budget; use Node syntax checks and a rendered-data smoke check.

### L3 — Delivery choice and T1 evidence
The user selected `Integración escalonada a main` (`stacked-to-main`). T1 adds 12 Chapter 6 exercise cards. `node --check` passed for the inline script; a static inventory found 12 Chapter 6 IDs with no duplicates. No focused pre-existing tests are available.
