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
Acceptance: Each new exercise includes a problem statement, rendered diagram, direct video suggestion from Videos FISICA, tip, step-by-step solution and final answer. Do not use YouTube search-result links or guessed URLs.
Checks: Exercise data-field completeness; every diagram key resolves to a real SVG generator.

### S4 — Study aids limited to this session's exercises
User request: "sería bueno complementar las mnemotecnias, flashcards y formulario con respecto y unicamente a los problemas que resolviste en esta sesión."
Acceptance: Add only formulas, mnemonics and flashcards relevant to the requested Chapters 6–7 problems; do not expand unrelated chapter aids.
Checks: Read back the new chapter-specific study-aid entries and confirm their formula coverage is exercised by the added problems.

## Tasks
- T1 — S1–S3: Add Chapter 6 exercises 6.10–6.27 with solutions, diagrams, direct videos and tips; route: inline; status: complete (12 requested IDs, SVG mappings, Node syntax, ID checks and direct video links passed); commits: `dec546a`, `147d301`.
- T2 — S1–S3: Add remaining requested Chapter 6 exercises 6.43–6.82; route: inline; status: complete (11 requested IDs; Node syntax, ID inventory, whitespace and direct video-link checks passed); commits: `1d53b35`, `147d301`.
- T3 — S1–S3: Add requested Chapter 7 exercises 7.39–7.56; route: inline; status: complete (9 requested IDs; syntax, ID inventory, diagram mapping, whitespace and direct video-link checks passed); commits: `239d5af`, `147d301`.
- T4 — S1–S3: Add requested Chapter 7 exercises 7.63–7.75; route: inline; status: complete (7 requested IDs; syntax, ID inventory, diagram mapping, whitespace and direct video-link checks passed); commits: `42e6970`, `147d301`.
- T5 — S4: Add session-scoped Chapter 6–7 formula reference, flashcards and mnemonics; route: inline; status: complete (both chapter topics added to all three study aids; Node syntax and whitespace checks passed); commit: `a11295d`.
- T6 — S1–S4: Validate all requested IDs, exercise fields, diagram mappings, inline JavaScript syntax and rendered page structure; route: inline; status: complete (exact inventories, all 39 cards/diagrams/required fields and direct videos render); commits: `a11295d`, `7ab5e07`, `147d301`.
- T7 — S3: Map direct Videos FISICA URLs to the requested exercises; route: inline; status: complete (39 mappings use direct user-provided watch URLs; no search links); commit: `147d301`.

## Log

### L1 — Original request (verbatim, trailing spaces removed for whitespace hygiene)
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

### L4 — T1 work-unit commit
Committed the Chapter 6 exercises 6.10–6.27 and their diagrams as `dec546a` (`feat: add chapter 6 energy exercises`). The repository reports receipt-driven development off at global scope; no native review or receipt was created.

### L5 — T2 evidence and source caveats
Added the remaining 11 requested Chapter 6 exercises. Syntax and ID checks pass (23 Chapter 6 IDs total, no duplicates), and `git diff --check` is clean. The recovered 6.44 materials conflict on population (6.5 × 10⁹ in the exercise versus 3.0 × 10⁸ in the solution calculation), so both results are shown. The Videos FISICA direct URLs could not be retrieved; no substitute search links are retained, and video links remain pending.

### L6 — T2 work-unit commit
Committed the remaining Chapter 6 exercises 6.43–6.82 as `1d53b35` (`feat: add chapter 6 power and spring exercises`).

### L7 — T3 verification
Added the first 9 requested Chapter 7 exercises. Node syntax validation passed, all 9 Chapter 7 IDs are unique, every exercise diagram key has a generator, and `git diff --check` is clean.

### L8 — T3 work-unit commit
Committed the Chapter 7 exercises 7.39–7.56 as `239d5af` (`feat: add chapter 7 energy exercises`).

### L9 — T4 verification
Added the remaining 7 requested Chapter 7 exercises. Node syntax validation passed, all 16 requested Chapter 7 IDs are unique, every exercise diagram key has a generator, and `git diff --check` is clean.

### L10 — T4 work-unit commit
Committed the remaining Chapter 7 exercises 7.63–7.75 as `42e6970` (`feat: add chapter 7 spring energy exercises`).

### L11 — T5 verification
Added Chapter 6–7-specific formula-reference topics, flashcards and mnemonic groups. Node syntax and `git diff --check` pass; source checks show one formula topic per chapter and matching flashcard/mnemonic groups.

### L12 — Final validation
An inline Node VM smoke test passed exact Chapter 6 (23 IDs) and Chapter 7 (16 IDs) inventories, all 39 required card fields and rendered SVGs, and rendering of the Chapter 6–7 formula reference, flashcards and mnemonics. `git diff --check` is clean.

### L13 — Study-aid work-unit commit
Committed the session-specific Chapter 6–7 formula reference, flashcards, mnemonics and final task evidence as `a11295d` (`feat: add chapter 6-7 study aids`).

### L14 — User correction: leave direct videos pending
User correction (verbatim): "entonces dejalo pendiente, no dejes eso que pusiste"
Removed the YouTube title-search links and video titles from the new exercise cards. Their video fields are now empty; direct URLs from Videos FISICA remain pending until they can be retrieved, with no search-page substitute.

### L15 — Video fallback removal verification
Node syntax and `git diff --check` pass. The rendered-data smoke test confirms the 39 new exercises have empty video arrays and no video-search UI, while existing direct video links, exercise content, SVG diagrams and study aids continue to render.

### L16 — Video fallback correction commit
Committed removal of the search-page links and unverified titles as `7ab5e07` (`fix: leave chapter 6-7 videos pending`).

### L17 — Retried NotebookLM MCP video-source lookup
The notebook and its 67-source count still resolve, but `list_sources`, `ask_notebook`, `get_source` and `find_source_by_title` all returned the Google account-routing `not found` error. No direct video URL was verified; T7 remains pending and the new exercises retain empty video arrays.

### L18 — User supplied direct video URLs
The user provided direct YouTube URLs from Videos FISICA; the requested exercises now use topic-matched direct links from that list, with no search-page substitutions.

### L19 — Direct video mapping verification
Node syntax and whitespace checks pass. The rendered-data smoke test confirms all 39 new exercises render direct `youtube.com/watch?v=` links from the supplied list and no YouTube search links remain.
