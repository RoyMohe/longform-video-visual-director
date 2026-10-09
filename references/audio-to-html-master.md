# Narration Audio to Editable HTML Master

This reference supplements the default editable storyboard-master contract in [established-editable-master.md](established-editable-master.md). Apply its audio-specific workflow whenever narration audio or a talking-head video is supplied; the user does not need to separately request HTML. Without audio, the main contract still requires the editable master with estimated timecodes.

## Source and timing

- Transcribe the supplied audio, preserve the spoken wording, and align every paragraph boundary to the source audio.
- Segment by viewer cognition and argument, not by subtitle line. Keep one logical narration paragraph per row.
- Store a reproducible character-to-audio alignment so later paragraph merges, splits, and text movement can recalculate timecodes without drifting downstream.
- Each row's play control must play only that row and stop automatically at its end.

## Primary deliverable

Create one self-contained local HTML master backed by local storage. The compact table columns are:

1. paragraph ID, editable timecode, approval/status, paragraph controls, and row audio controls;
2. one or two storyboard-image slots, expandable only when the user requests more;
3. full editable narration paragraph;
4. narrative/visual function;
5. picture and composition;
6. motion and edit;
7. asset, source, rights, and production note.

Include a sticky header with the source audio player, prominent audio realignment control, undo, redo-queue export, JSON import/export, and print/PDF. Include the established full-video rhythm overview and duration-based L1/L2 visual-mix summary; do not silently omit them from a new master.

## Required interactions

- Autosave edits locally and preserve imported revisions.
- Support paragraph add, merge, reorder, and storyboard-slot add/remove.
- Support Ctrl+Z and a visible undo control across text, timing, structure, storyboard count, confirmation, import, and queue actions.
- Give every row matching, same-size controls for play/pause and restart-from-row-start. Move the playing-row highlight immediately when another row starts or restarts; stop at the row end.
- Put the audio realignment control directly beside the main audio player. Give exact, approximate, or failed-match feedback.
- After narration resegmentation, mark only affected visual rows as needing sync and show overlapping source rows. Queue only the rows the user explicitly confirms.
- Export a deterministic redo-queue JSON because a standalone local HTML file cannot directly wake or message the current Codex task.

## State and regeneration

- Treat the browser-edited master as authoritative over earlier chat text and baseline files.
- Apply completed redo batches through an idempotent migration keyed to row ID, current timecode, and current narration. Record the synced narration/timecode signature so later audio recalculation does not restore stale warnings.
- Preserve unlisted rows, accepted images, storyboard count, and unrelated edits.
- Never embed a generated storyboard image as accepted. Insert only after explicit user acceptance; otherwise label it draft, pending, or needs redesign.

## Storyboard generation

- Generate frames in the accepted episode aspect ratio, aligned to the exact row and storyboard slot; use 9:16 only when that is the episode brief.
- Treat every storyboard image as a **video keyframe**, never as a self-contained product poster, infographic page, presentation slide, or thumbnail. It represents one readable instant inside an edit and must leave room for motion before and after it.
- When the episode is presenter-led, keep the presenter present throughout the video. In draft storyboards, use a portrait/avatar stand-in unless an exact source-video frame is needed. The presenter's crop, frame shape, scale, and left/right position are composition-dependent rather than fixed: use a circle, rounded rectangle, document inset, masked half-body, or full presenter shot as the visual hierarchy requires. The presenter may be temporarily covered by a source clip but remains the recurring anchor. The hard constraint is vertical safety: never park the presenter against the bottom edge or inside the lower subtitle-safe region; keep the lower 20% available for the default subtitle system.
- Do not bake the ordinary spoken subtitle layer into storyboard images. Narration subtitles use the video's default subtitle system and are added in edit. Only include text that belongs to the visual itself: one indispensable keyword, one large number, a short label, or legible source-document text.
- Use a one-glance readability test. At phone size, the viewer should understand the frame's dominant subject and visual relationship in under one second. Avoid dense small copy, feature lists, multiple explanatory paragraphs, poster footers, legends, decorative UI chrome, and redundant headings.
- For reference creators, extract transferable principles such as presenter anchoring, simple flat source layers, document/footage windows, bold single-point emphasis, and editorial rhythm. Do not imitate a creator's recognizable layouts shot for shot.
- Prefer real footage, screenshots, documents, maps, charts, product shots, and simple flat graphic packaging over fully synthetic poster compositions. A frame may combine presenter + one main source layer + one emphasis device; add more only when the narration genuinely compares several items.
- For presenter-led editorial videos, default to **designed 2D packaging**, not generated environments: keep the real presenter plate visible and build the idea from separately animatable cards, crops, charts, documents, logos, product cutouts, icons, lines, arrows, brackets, large numbers, color blocks, and short emphasis labels. Depth should normally come from scale, masks, shadows, overlap, and light parallax. Do not turn an abstract claim into a photorealistic room, laboratory, vault, data center, hologram, or other synthetic 3D scene merely to illustrate the noun.
- Here, **2D means a layered editorial composite, not flat-vector illustration**. Preserve the photographic texture of real footage, screenshots, documents, products, and portraits; add restrained material differences, edge highlights, masks, tonal grading, blur, grain, perspective offsets, shadows, reflections, and depth-of-field. Avoid childish icon sets, thick bright outlines, oversized rounded rectangles, cartoon diagrams, generic app-dashboard cards, and loud candy colors unless the reference explicitly calls for them.
- Every storyboard frame must imply a practical layer stack and motion path. The editor should be able to identify which element enters, exits, scales, highlights, flips, draws on, or gets replaced. If the proposed frame cannot be decomposed into source footage plus editable 2D layers, mark it as an exceptional hero shot rather than the default treatment.
- Reserve 3D, bespoke spatial scenes, and generative environments for rare story-critical hero moments or when the user explicitly requests them. A reference dominated by flat presenter packaging must not be translated into a batch of AI-generated scenes.
- Prefer a representative 60–90 second pilot before full-episode image generation when the visual language or production density is not yet accepted.
- Start a new visual direction with only 2–3 representative sample frames. Do not generate the rest of the pilot until the user approves presenter scale, information density, and packaging style.
