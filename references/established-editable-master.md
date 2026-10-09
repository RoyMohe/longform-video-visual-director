# Established editable storyboard master
This is the user's previously agreed deliverable contract, not a new layout inferred from one screenshot. Use it for every episode-script request under this skill unless the user explicitly asks for another format. Do not require an audio upload, an HTML request, or a reminder about tables before applying it.

## Primary delivery
- Deliver a local editable HTML storyboard master plus revision JSON. Markdown scripts and editor cut lists are supplements, never replacements.
- Use one logical narration paragraph per row, stable paragraph IDs, editable start/end timecodes, full verbatim narration, visual function, picture/composition, motion/edit, and asset/source/production notes.
- Give each row one representative frame or two frames for a meaningful start/end contrast. Show actual storyboard keyframes aligned to the paragraph and slot; a file link, text-only frame description, blank image column, or unrelated stock thumbnail does not fulfil a finished storyboard delivery.
- Preserve the existing sample-first approval workflow for a new visual direction: show 2–3 representative draft frames first; retain pending slots for the rest and explicitly say that the first pass is not the finished image set. Never bypass approval by filling every row with unapproved generated images.
- Genuine artwork/footage crops may serve as storyboard keyframes when they show the directed composition. Label source crops as reference/draft; do not substitute raw full-image thumbnails for designed keyframes when the shot requires composite layers.
- Status is per slot: accepted/confirmed only after explicit user acceptance, otherwise draft/pending/needs redesign. Preserve accepted frames and unrelated rows during any update.
- Keep the seven-column compact mother table, not a sentence-by-sentence or 3–8-second cut-list table. Keyframes are not the actual source-cut count.

## Header and overview
- Sticky project header: title/version, aspect ratio, presenter mode, timing basis, full runtime, paragraph count, planned cut count, frame configuration, autosave state.
- Audio player and realignment control directly adjacent when source audio is available; undo, redo-queue export with count, revision JSON export/import, print/PDF, and recoverable baseline restore.
- Full-video rhythm timeline with chapter/paragraph boundaries and planned internal cut points. Clicking a point locates the relevant row and seeks source audio when available.
- Compute L1/L2 visual-mix percentages from planned duration, with a declared convention for mixed shots. Do not invent counts or measured percentages.
- Use the established dense working-table UI: dark surface, off-white text, restrained lime status/action highlights, fixed table header, time/control and storyboard columns remaining visible during horizontal scrolling. Episode art direction belongs inside the storyboard and does not replace the workbench.
- Aspect ratio follows the accepted episode brief; no universal 9:16 or 16:9 lock.

## Interactions and persistence
- Direct cell editing with localStorage autosave and portable JSON import/export. Persist timing, narration, structure, frame slots/status, visual edits, and queues.
- Row controls: play/pause, restart from row start, move up/down, merge, add paragraph, add/remove storyboard slots. Undo/Ctrl+Z covers text, timing, structure, slot changes, import, queue and confirmation actions.
- Row playback ends automatically at its end; highlight follows the currently playing row immediately.
- Never show confirm/regenerate controls on untouched rows. Editing picture/composition or motion/edit reveals a button directly beneath the field just edited.
- Confirmation queues only that paragraph's affected one/two storyboard slots. Narration/function/asset edits autosave without implicit image regeneration; narration/timing changes may mark affected rows for sync.
- Export only explicitly confirmed redo tasks. A standalone HTML file cannot wake this chat or call generation by itself; state the actual handoff.
- Treat browser revisions/imported JSON as authoritative. Read the latest master before regenerating; apply updates idempotently by row ID plus timing/narration signature. Preserve unlisted rows, all accepted images, frame counts and unrelated edits.
- Without audio, deliver the same complete table with estimated/editable timings. Show “未提供音频 / 时间码暂定”; disable unavailable audio controls with an explanation. Do not invent a playable source, waveform, exact alignment, or cut-to-audio precision.
- With audio, apply the full alignment and playback rules in [audio-to-html-master.md](audio-to-html-master.md). Approximate reweighting must be labelled approximate and must not replace exact timing silently.

## Continuity with existing masters
If an established master exists for the episode, update it rather than create a simpler replacement. The user's existing Token/Babel master demonstrated this interface and workflow; its topic, 77 paragraphs, 16:9 ratio and episode palette are not universal defaults. Do not reduce the established interaction contract to the appearance of a screenshot.

## Delivery checks
Open/render the actual HTML and check table/timeline layout, image paths, row/slot counts, full narration coverage, editable timing, autosave/reload, import/export, undo, structure controls, conditional confirmation and single-row queue preservation. Check audio seeking and automatic row stop only with real source audio. Report draft/pending frames and unavailable dependencies accurately; do not call a text-only outline a completed storyboard master.
