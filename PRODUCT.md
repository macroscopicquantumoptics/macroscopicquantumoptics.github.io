# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

A balanced mix, served equally:

- **Prospective members**: doctoral, master's and postdoc candidates deciding whether the group fits them and whether to write to the group leader (Anton Zasedatelev).
- **Fellow researchers**: collaborators, referees and conference contacts checking the group's papers, people and research directions.

Secondary: funders, press and Aalto colleagues. Group members are also users as maintainers: they edit pages by hand and post news.

## Product Purpose

The public website of the Macroscopic Quantum Optics (MQO) group, Department of Applied Physics, Aalto University. It says what the group studies, who is in it, what it has published and built, and how to join.

Success means:

- strong candidates write to the group about positions and thesis projects;
- papers, people and research directions are easy to find and cite;
- the group's open tools (levtrap, PlotBench, QUOP Tabletop) reach other labs;
- any group member can keep it current in a plain editor, without help.

## Positioning

An experimental quantum optics group working on three directions: correlated quantum states of light and matter (exciton-phonon systems in high-Q cavities), nonequilibrium Bose-Einstein condensates (polariton condensates, all-optical logic), and quantum control of large-mass motion (levitated optomechanics, hybrid RF and dark optical trap in UHV). The home page shows this through interactive 3D models of the group's own experiments, each tied to its paper.

## Operating Context

- News is posted on LinkedIn first; chosen posts become news items via `tools/linkedin_news.py` or the "News from LinkedIn" GitHub Actions workflow, then reviewed in a pull request.
- Pages are edited by hand and published by pushing to `main` (GitHub Pages).
- The site's look matches the group meeting slides; both follow the Aalto brand guidelines.
- Related outside presences: group page on aalto.fi, QCLM conference (qclm.fi), LinkedIn, GitHub (github.com/macroscopicquantumoptics).

## Capabilities and Constraints

- Plain HTML and one CSS file. No build step, no Node, no frameworks, no CDNs. three.js r170 is vendored in `assets/vendor/three/` for the home page models; Inter is bundled.
- Pages: home, research, people (with one profile page per person), publications, news, resources, positions (`join/`), 404.
- Header and footer are repeated on every page and must be changed everywhere together.
- Light and dark themes, user toggle; the home page 3D picture falls back to a video where WebGL is missing, and respects reduced motion.
- AGENTS.md is the maintainers' guide and holds the detailed editing and look rules; keep it and this file consistent.

## Brand Commitments

Binding, as written in AGENTS.md:

- Aalto brand guidelines: Inter, black on white / white on black, School of Science yellow `#F7E159` as the only highlight, never yellow text on white. Flat: no cards, boxes, shadows, gradients, rounded corners, chips, icons on links. Three type sizes, sentence case, one left edge.
- MQO logo (separate light and dark files) top left; Aalto logo top right, never cropped, recoloured or stretched.
- Writing: plain and specific; say what the group does and what happened. No invented results, numbers, people or dates. No filler ("cutting-edge", "at the forefront", "we are passionate about"), no em dashes as sentence glue.

## Evidence on Hand

- Real portraits in `assets/people/`, news pictures in `assets/news/`, tool screenshots in `assets/resources/`.
- 3D models and a dark-trap video loop based on the group's papers (PRL 133, 186903; arXiv:2601.15080; arXiv:2508.10809; `dark_trap_cover.blend`).
- Publications list, news archive and three open tools with live pages and code.
- No testimonials, metrics or rankings exist; do not invent them.

## Product Principles

1. Show the science itself (experiments, papers, tools) rather than describe how good it is.
2. A candidate should always be one step from knowing how to apply.
3. Every page stays editable by hand by a group member; no change may need a build or a specialist.
4. Stay inside the Aalto brand so the site, slides and university pages read as one family.
5. Accuracy over polish: every name, date and claim is real and current.
