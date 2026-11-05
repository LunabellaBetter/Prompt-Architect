---
name: kid-sticker-gif-series
description: Create a consistent character model from authorized reference photos, then produce one expressive, independently usable animated GIF sticker at a time. Covers character modeling, visual-system continuity, storyboarding, frame generation, GIF assembly, QA, and public/private asset separation.
---

# Kid Sticker GIF Series

## Mission

Create a coherent personal sticker series from an approved character model. The workflow covers the complete chain: reference-photo analysis, character prototype, model-sheet approval, expression storyboard, single-sticker animation generation, deterministic GIF assembly, frame-by-frame QA, and controlled asset storage.

## Non-negotiable rules

- One expression equals one independent GIF file.
- Produce one sticker per task and review it before starting the next.
- Each GIF contains one expression theme, one character performance, and at most one caption.
- A contact sheet, 4×4 sticker sheet, horizontal strip, scrolling sequence, or sprite sheet is never a final sticker deliverable.
- Sprite sheets may be used only as internal animation sources and must be cropped into individual frames before final assembly.
- A subtle head wobble alone does not count as expressive animation.
- Meaningful changes must be visible in facial expression, hand gesture, body posture, or emotion props.
- The approved character model sheet controls identity. Do not let the character drift between stickers.
- If an image-generation or file-processing tool fails, report the failure and stop. Do not silently retry or substitute unrelated images.

## Privacy and publication boundary

### Public-safe material
- Brand-neutral production instructions and reusable prompts.
- Neutral visual-style summaries.
- Generic user-created HRBP animation references without company names, logos, values, confidential content, or identifiable employees.
- Synthetic examples and generic QA procedures.

### Private-only material
- Child reference photos, child-derived model sheets, and the child's finished sticker series.
- Company-branded or company-specific HRBP sticker references.
- Stickers containing company values, slogans, brand names, logos, uniforms, or company-specific identifiers.
- Internal source material or assets with unclear publication rights.

Never commit a child's original photos to a public repository. Keep original photos outside GitHub unless the parent or guardian has explicitly authorized that storage and sharing. The public Skill must remain brand-neutral.

## Stage 1 — Character prototype

### Analyze the reference set
Separate stable identity cues from temporary photo details. Record face silhouette, eye shape and spacing, eyebrow/nose/mouth language, hair silhouette and parting, stable accessories, outfit only when it is intended to remain fixed, and the overall age-appropriate character impression.

Do not turn transient lighting, camera angle, background, or unrelated props into permanent character traits.

### Create a model sheet
Create one reference sheet with front, three-quarter, and side views; a neutral expression; and a small set of useful expression studies. A model sheet may contain multiple views because it is a continuity reference, not a chat sticker.

### Review and lock
Ask the user to review face proportions, hair silhouette, facial features, outfit, signature markers, and overall resemblance. Only after explicit approval, mark the model sheet as the approved anchor and version it, for example character-model-v0.1. Any later identity change requires a new version and a change note.

## Stage 2 — Visual system

Use the saved Notion cards as a coordinated system, with each card contributing only its intended role.

- S36 Soft Picture-book Illustration: controls the character rendering language—rounded simplified forms, slightly irregular black hand-drawn outlines, restrained facial features, gentle blush, warm cream and muted pastel colors, light paper grain, sparse doodles, flat illustration, minimal shadow.
- S37 Chinese Mouse-doodle Chat Stickers: contributes loose line energy, spontaneous hand-written Chinese captions, uneven visual rhythm, and playful chat-sticker humor. Its original 4×4/16-sticker layout is not used for final delivery.
- S38 Multilingual Mouse Doodle: contributes language adaptation and playful hand-written caption treatment. Keep the requested language readable.

Priority order:
1. Approved character model sheet.
2. S36 character-rendering direction.
3. S37/S38 doodle and caption language.
4. Approved animation references for motion grammar.
5. Current sticker-specific storyboard.

The Notion cards were marked pending visual validation when read. Treat them as user-maintained inspiration, not as independently verified commercial licenses or proven rendering recipes.

## Stage 3 — One-sticker storyboard

Before generation, write a four-beat performance script. Each beat must specify eye state and gaze, eyebrow shape, mouth shape, hand/arm gesture, head or torso posture, optional emotion props, and what changes from the previous frame.

A useful four-beat structure:
1. Set-up: establish the emotion.
2. Build: intensify or reveal it.
3. Peak: strongest expression or gesture.
4. Release: settle into a loop-compatible pose.

Four frames are the default. Use more only when the action genuinely needs intermediate poses.

## Stage 4 — Generate one animation source

Generate only the current sticker. Preferred source structure is a 2×2 grid for four frames, equal cell dimensions, one pose per cell, stable character scale and camera distance, character fully inside each cell, and no borders, gutters, labels, numbering, or multiple sticker themes.

Prefer a transparent background. Do not ask the image model to generate several sticker concepts in one request.

### Caption handling
Prefer generating the character animation without text, then add the exact caption as a separate stable overlay during post-processing. This prevents misspelled, duplicated, or changing Chinese text.

If text is generated inside the image, inspect spelling, punctuation, position, and duplication in every frame. Reject malformed or changing text.

## Stage 5 — Assemble a real GIF

A generated preview may show a sprite sheet. Treat it as source material until the actual output file has been inspected.

When the source is a sprite sheet:
1. Crop each cell using exact grid coordinates.
2. Normalize all frames to one canvas size.
3. Align the character using stable anchors such as head center and torso baseline.
4. Preserve transparent pixels and avoid white/cream halos.
5. Add the caption once as a stable layer, if needed.
6. Assemble frames into one looping GIF.
7. Set timing according to the action, not a fixed duration for every sticker.
8. Optimize file size without destroying line quality or facial detail.

Suggested starting point: 512×512 canvas, four frames, 180–320 ms per frame for ordinary reactions, infinite loop, transparent background. Faster actions may use shorter timing; sleep or emotional holds may use longer timing.

The final GIF must be inspected as an animated file. A PNG/JPG sprite-sheet preview is not a GIF deliverable.

## Stage 6 — Mandatory QA

### Identity
- Same face, hair silhouette, outfit, and signature markers.
- No age, hairstyle, accessory, or clothing drift without approval.
- Never copy the adult character identity from HRBP reference GIFs into the child character.

### Expression
- The emotion reads immediately without relying on the caption.
- At least two meaningful expression/action dimensions change.
- Eyes, eyebrows, and mouth are checked explicitly.
- Hands or body posture contribute when the emotion calls for them.

### Motion
- Frames show real performance, not a static head with minor jitter.
- Motion progresses logically from set-up to peak to release.
- No abrupt character-scale jumps or unwanted frame shifts.
- The loop returns cleanly to the opening pose.
- No unintended duplicate frames that make the action appear frozen.

### Artifact
- File opens as GIF and contains multiple frames.
- Frame durations and infinite loop are present.
- Transparency is retained.
- One canvas size is used throughout.
- Exactly one sticker theme and at most one caption appear.
- No collage, horizontal strip, or multi-sticker grid appears in the final file.

Automated metadata checks cannot judge whether the sticker is genuinely expressive. Play the GIF at normal speed and inspect every frame. User acceptance is the final visual gate.

## Stage 7 — Delivery protocol

Deliver one sticker at a time:
- Show the actual animated GIF.
- Provide its standalone file.
- State expression name and frame count.
- Report any known limitation.
- Ask for acceptance or correction.

Do not bundle a series into a ZIP until each individual sticker has passed review. A contact sheet may be supplied separately for overview, clearly labeled as a static preview.

## File naming

Use stable sortable names such as 01_expression-name.gif and 02_expression-name.gif. Keep source sheets, cropped frames, QA records, and final GIFs in separate folders.

## Completion definition

A sticker is complete only when the approved character identity is preserved, the expression is immediately legible, the animation contains meaningful coherent movement, the file is a standalone transparent looping GIF, the file contains one sticker only, and the user accepts it.
