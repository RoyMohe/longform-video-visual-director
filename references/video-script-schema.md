# Timecoded Video Script Schema

The script must bridge editorial intent and production execution. Keep narration verbatim unless rewriting is authorized. The primary artifact is the previously agreed editable HTML storyboard master defined in [established-editable-master.md](established-editable-master.md), even for short episodes and narration text without audio. The Markdown tables below describe its fields; they do not replace the HTML delivery.

## Direction header

Include estimated or target duration and timing basis, format/aspect ratio, episode visual thesis, connection to the account visual bible, episode motif and its opening-to-ending evolution, production level and constraints, and factual/sourcing/rights assumptions.

## Beat map

Before the detailed table, summarize the episode in narrative beats:

| Beat | Time | Narrative function | Viewer question/feeling | Visual function | Motif state |
|---|---:|---|---|---|---|

Use natural argument units. Do not force a predetermined beat count.

## Detailed timecoded table

Account for the full narration using rows that are practical editing units:

For storyboard review, use logical narration paragraphs and one or two keyframe slots per row. Do not create a keyframe for every sentence. Use one keyframe for a stable idea/state and two for a meaningful entering-to-ending change. Treat this as an approval artifact, then derive the finer editorial cut list separately when needed.

In an editable storyboard master, keep untouched rows free of confirmation controls. Reveal a row-level confirm-and-regenerate action only after picture/composition or motion/edit has changed. Confirmation must queue regeneration for that row alone and preserve all other rows and accepted images. Other text fields may autosave without triggering storyboard regeneration.

| TC / duration + status | Accepted storyboard | Narration | Narrative job | Picture and composition | Motion / edit | On-screen text | Sound | Asset / source / production note | Revision note |
|---|---|---|---|---|---|---|---|---|---|

Use `accepted`, `draft`, `pending`, or `needs redesign` as explicit row status during iteration. Embed an image only after the user has accepted that frame. Keep rejected or merely generated images out of the accepted-storyboard column.

Each row should answer:

- exactly which narration span it covers;
- the primary visual function: Anchor, Prove, Explain, Evoke, Orient, or Release;
- what is visible, foreground/background relationship, scale, framing, depth, light, and relevant color behavior;
- presenter action or eyeline when applicable;
- object and camera motion, cut logic, transition meaning, and the state at the end of the shot;
- exact on-screen copy, hierarchy, placement, and dwell behavior;
- dialogue, music, ambience, SFX, and intentional silence;
- asset origin and production path: shoot, screen-record, research, license, design, animate, composite, or generate;
- evidence status and any source verification needed;
- production tier L1, L2, or L3 when useful.

When the user edits the table directly, preserve those edits as the current script authority. Recalculate affected timing and downstream continuity without overwriting unrelated accepted rows.

Avoid vague lines such as “科技感画面,” “快切素材,” or “配相关 B-roll.” Name the subject, action, relationship, and reason for the shot.

## Timing

If final narration audio exists, use its timings. Otherwise estimate from text length and stated delivery style, label all timecodes as draft, and preserve enough elasticity for performance. Do not imply frame accuracy without audio.

Shot duration should follow comprehension. Documents and charts need readable holds; emotional consequences often need air; simple orientation cards can be brief. A row may contain a purposeful micro-sequence if listing every cut would make the production script less usable.

## Evidence and graphics specifications

For a factual screen, specify the claim, needed source, exact crop/highlight or chart encoding, labels/units/date range/citation placement, and whether the image is authentic, recreated, conceptual, or generated.

For explanatory graphics, specify initial state, transformation, final state, and takeaway. For UI, specify device/context, interaction path, cursor/touch behavior, and privacy redactions.

## Consolidated production list

After the script, group requirements into presenter/location shots; archive/documents/data/research captures; UI/product screen recordings; editorial stills/footage; custom 2D/3D/motion graphics; optional generated assets; music/ambience/SFX; and unresolved rights/facts/technical dependencies.

For each significant item give owner/type, quantity or approximate duration, production tier, and dependency. End with the highest-risk items and a feasible fallback for each.
