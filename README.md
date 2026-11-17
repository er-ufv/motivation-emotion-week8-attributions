# Motivation & Emotion · Week 8: Why did it happen?

**Self-paced, gradable web activity in Spanish for the course *Motivation and Emotion*, Week 8. It covers causal attributions, learned helplessness, explanatory styles and perceived control. An animated teacher avatar guides the session, students work through four realistic cases, answers are scored automatically, and students download a PDF to submit on Canvas.**

> Actividad autónoma y evaluable (en español) de *Emoción y Motivación*, Semana 8: atribuciones causales, indefensión aprendida, estilos explicativos y control percibido.

The activity is a single self-contained `index.html`. The avatar animations, figures, logo and the PDF library are all embedded, so it needs no server or build step and can be published as it is with GitHub Pages.

## Session flow (100 minutes, individual)

| Block | Steps | Planned time |
|---|---|---|
| **Block 1** | Reading (lecture notes, week 8, pp. 11–20) → guided tour (4 short capsules with the avatar) → Case 1 | 20′ + 15′ + 15′ |
| *Break* | Full-screen break screen with a 10-minute countdown | 10′ |
| **Block 2** | Cases 2, 3 and 4 → submission (PDF download) | 13′ + 13′ + 14′ + 10′ |

## Features

- Welcome screen in which the avatar apologises for being absent, followed by a comic-style guided explanation that uses several avatar expressions.
- Four cases:
  - **Case 1:** the class group chat after an exam (Weiner's attributions and the emotions that go with them).
  - **Case 2:** a debate team that is knocked out of a tournament (explanatory styles).
  - **Case 3:** an employee with learned helplessness.
  - **Case 4:** a swimmer who wants to quit vaping (self-efficacy, outcome expectancy, self-esteem and perceived control).
- A per-step timer with warnings when a student goes over the planned time, plus a break screen at the end of Block 1.
- A searchable glossary in a side panel.
- On finishing, answers lock and the scored answer key is shown. A floating warning button points students to the PDF download.
- The PDF includes the student's details, start and submission times, the reading declaration, the scores for the closed questions, the answers with corrections, and the open answers for the teacher to grade.

## Publish on GitHub Pages

1. On GitHub, create a **new public repository** named `motivation-emotion-week8-attributions`.
2. In the **About** box, paste the description from the first paragraph above. Suggested topics: `education`, `psychology`, `motivation`, `attribution-theory`, `github-pages`, `canvas-lms`.
3. Go to **Add file → Upload files** and drag in **every file in this folder**: `index.html`, `README.md`, `LICENSE`, `.nojekyll` and the `assets/` folder. Then commit.
   - `.nojekyll` is hidden in macOS Finder; press `Cmd + Shift + .` to show it. The site still works without it.
4. Go to **Settings → Pages**, choose **Deploy from a branch**, then `main` / `(root)`, and **Save**.
5. After a minute or two the site will be live at `https://YOUR-USERNAME.github.io/motivation-emotion-week8-attributions/`.

`assets/avatar.png` is the avatar picture used by the Canvas announcement.

## Configuration

Edit the `CONFIG` object at the top of the main `<script>` in `index.html`:

| Key | Purpose |
|---|---|
| `tareaCanvas` | Name of the Canvas assignment where students upload the PDF. |
| `enlaceTareaCanvas` | URL of that assignment. When set, an «Ir a la tarea de Canvas» button appears at the end. |
| `segundosBienvenida` | Duration of the welcome screen, in seconds (default 10). |
| `minutosDescanso` | Length of the break, in minutes (default 10). |
| `tiempos` | Planned minutes for each step. These drive the timing warnings. |
| `mostrarSolucionesEnPDF` | Set to `false` to mark answers right or wrong in the PDF without revealing the key. |
| `puntosCerradasPorCaso` / `puntosAbiertaPorCaso` | Score weights (default 2 + 0.5 per case, 10 in total). |

## Notes

- Answers are kept only in memory. If a student reloads or closes the tab, their answers are lost; the activity warns students about this.
- Because the page runs without a server, the answer key is inside the source code. The open questions, which the teacher grades, carry part of the mark for this reason.
- The page is best viewed on a laptop or tablet. It works on phones, and phone users see a notice recommending a larger screen.

## Licence

- **Code:** MIT (see `LICENSE`).
- **Teaching content** (texts, cases, figures and avatar): CC BY-NC-SA 4.0.
- Characters and cases are fictional.
- Includes jsPDF 2.5.2 (MIT).

Author: Eduar Ramírez · 2026
