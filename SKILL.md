---
name: life-kline
description: Create vertical short videos that tell a historical figure’s life through a growing candlestick chart, event captions, and optional sound design. Use when a user wants a biographical K-line animation or a reusable visual story built from life events.
---

# Life K-line video

Turn verified life events into a continuous candlestick chart. Price movement is a storytelling metaphor, never historical data or an objective score of a person.

## Workflow

1. Read the visual reference or inspect the supplied video. Separate chart layout, event rhythm, candle behavior, camera movement, captions, and sound. Do not infer motion from a still image.
2. Research the subject’s dates and major events using reliable sources. Record citations in the project spec. Label uncertain or disputed details instead of presenting them as settled facts.
3. Draft a beat sheet before rendering. Give each beat one meaningful change: a decision, setback, battle, achievement, exile, return, or death. Use fixed beat lengths only when requested; total duration follows the number of useful beats. A quiet or plateau section can still reveal a new event.
4. Map the story to a continuous value path. Use rises, pullbacks, limits, plateaus, rebounds, and ending states to emphasize narrative turns. Keep the line continuous across beats. Label the chart as a narrative metaphor and never present its numbers as factual measurements.
5. Copy `assets/example.json` and adapt the person, events, captions, sources, duration, and price path. Set `brand` to `林序聊AI` unless the user requests a different brand. Use the chart template in `assets/index.html` for the standard short sample. For a longer event sequence, adapt the template to the actual beat count and duration; do not reuse a fixed-duration renderer without updating its timing and camera calculations.
6. Render with local FFmpeg and Playwright Chromium. The helper accepts `--spec`, `--out`, and optional `--fps`; pass `--ffmpeg` if FFmpeg is not on PATH. Install Python dependencies in the target environment as needed. The renderer produces an MP4 and review frames.
7. Review the contact sheet and key frames for title/caption readability, chart continuity, event order, and brand placement. Confirm duration and whether an audio stream exists. Fully decode the exported video before delivery.

## Sound

Audio is optional. Do not add music or narration unless requested. If using a supplied reference track, keep it local and never package it with the public skill. Extract only what the user requested and has rights to use. When designing sound to follow the chart, make rising and falling pitch respond to the same value curve as the candles; use smooth transitions so each beat does not sound like a disconnected alert. State clearly whether the result uses extracted source audio, newly generated sound, narration, or silence. Never claim a track is aligned or voice-isolated without checking it.

## Boundaries

The included templates draw geometry and text; they do not require an image-generation model. Portraits require user-provided assets or a separately available image tool. Do not copy platform UI from a reference video. Do not include private project paths, personal recordings, credentials, or user-specific archives in a public repository.

Copyright and project license are documented in the repository root. Copyright line: `© 林序聊AI (linxu聊AI)`.
