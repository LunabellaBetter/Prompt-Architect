# GIF technical QA

| Check | Acceptance |
|---|---|
| Container | Opens as an animated GIF. |
| Frame count | More than one frame; normally four. |
| Canvas | Identical dimensions across frames. |
| Loop | Infinite loop (loop=0). |
| Transparency | Transparency index present; no unintended opaque canvas. |
| Timing | Per-frame duration matches the storyboard. |
| Composition | One character performance and one expression theme only. |
| Caption | Exact wording; one stable caption layer at most. |
| Motion | Distinct meaningful frame-to-frame change. |
| Loop seam | Last-to-first transition is intentional and visually clean. |

## Recommended processing sequence
1. Inspect source dimensions, alpha, frame count, and grid structure.
2. Crop each source cell independently when using a sprite sheet.
3. Align character scale and stable anchors.
4. Normalize canvas dimensions and transparent padding.
5. Composite a fixed caption layer if required.
6. Convert to a GIF palette while preserving a transparent index.
7. Set frame durations, disposal, and infinite loop.
8. Reopen the saved GIF and inspect the actual frames.
9. Play it at normal speed.
10. Record QA status and file hash.

Metadata can prove that a file is animated; it cannot prove that the expression is convincing. Reject files that only wobble, duplicate near-identical frames, drift in scale, lose character identity, or combine multiple stickers.
