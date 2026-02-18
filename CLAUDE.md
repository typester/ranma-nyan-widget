# CLAUDE.md

## Language

- All generated output must be in English unless explicitly specified otherwise.

## Version Control

- Use `jj` for version control (not git).
- Write operations (commit, push, etc.) are done by the user unless explicitly instructed otherwise.

## Code Style

- Keep code comments minimal. Only add comments where the logic is genuinely unclear.
- Never add comments that merely restate what the immediately following code does.

## Memory

- Persist anything that should be remembered across sessions by updating AGENTS.md or CLAUDE.md.

## Plan Mode

- Every plan must include "Step 0: Re-read AGENTS.md and CLAUDE.md" to ensure guidelines are fresh.

## Feedback Handling

- When the user provides feedback or reports issues with generated output, do NOT edit code immediately.
- Instead: investigate the issue, then enter plan mode to propose a fix. Editing without explicit plan approval is prohibited.

## Project Notes

- This is a ranma widget. Follow conventions from `../ranma/examples/pixel-runner/`.
- Single plugin file: `plugins/nyan_cat.py`. Pure Python 3 stdlib only (no Pillow).
- PNG generation uses `make_png()` (struct + zlib).
- Scene: 140×15 source pixels, rendered at `image_scale=1` (140×15 displayed).
- Cat sprite: 25×15 pixels from nyan-mode XPM (GPL-3.0), 6 frames.
- Rainbow: 15 bands × 1px with baked-in wave (per-frame colors from XPM column 0).
- Temp files in `/tmp/ranma_nyan_cat/`, atomic writes via `os.replace()`.
- Data sources: `--source cpu` (default), `--source battery`, `--source stdin`.
