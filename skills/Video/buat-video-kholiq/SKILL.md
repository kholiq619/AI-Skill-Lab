---
name: buat-video-kholiq
description: Produces a finished short-form video from a topic, title, brief, or supplied narration. Use when the user types /buat-video or asks to create/render a video directly.
---

# /buat-video — Kholiq Visual Lab

## Mission
Turn the user's supplied topic, title, brief, or narration into a finished short-form video with the fewest possible conversational turns. Treat `/buat-video` as an execution command, not a request for brainstorming.

## Invocation and input
The user may provide:
- `/buat-video <topic or title>`
- `/buat-video <full narration>`
- `/buat-video <brief> [attached audio, images, clips, or reference files]`

Immediately inspect the current conversation and available attachments. Reuse relevant material already supplied. Do not ask the user to repeat information already present.

## Non-negotiable interaction rules
1. Start work immediately. Do not greet, praise the idea, explain your plan at length, offer alternatives, or ask for approval of ordinary creative choices.
2. Do not return only an outline, storyboard, script, or code when video rendering is possible. Produce and render the actual video.
3. Make reasonable creative decisions yourself: hook, scene order, visual metaphors, motion, transitions, typography, sound design, pacing, and export settings.
4. Ask a question only when a missing item genuinely blocks production and no safe, sensible fallback exists. Ask one concise question, not a questionnaire.
5. If the user supplies narration, preserve its wording. Do not rewrite, shorten, or embellish it unless explicitly requested.
6. If the user supplies a topic/title but no narration, write a concise, factual narration suitable for the target duration and use it as the production script. Do not pause for approval.
7. Never invent facts, statistics, quotations, names, brands, events, or source claims. If the topic requires current facts, research them when tools permit and cite them in the accompanying note; otherwise clearly avoid unsupported specifics.
8. Do not claim an export succeeded until the final file exists and has been checked.
9. If a render or tool call is interrupted by a limit, preserve the project and exact progress. On continuation, resume from the last completed step; do not restart or duplicate work.
10. Do not expose lengthy internal reasoning. Keep the final response concise.

## Production workflow
### A. Parse the request
Determine from context:
- Topic/title or supplied narration
- Platform and aspect ratio, defaulting to vertical 9:16 for Reels/Shorts/TikTok
- Target duration, defaulting to 30–60 seconds unless the narration dictates otherwise
- Language, defaulting to the user's language
- Existing audio, images, video clips, brand assets, and style references

Do not ask about defaults. Choose sensible values and proceed.

### B. Prepare content
- If narration is supplied, use it verbatim.
- If only a topic/title is supplied, create the hook, narration, and scene plan internally.
- Make the opening visually compelling within the first 1–2 seconds.
- Keep each scene purposeful; avoid repetitive stock-like sequences and generic filler.
- Use on-screen text sparingly and ensure it is readable on a phone.
- Match every visual claim to the narration and available evidence.

### C. Audio
Priority:
1. Use the user's attached/supplied voiceover.
2. If the user explicitly provides a generated voice file, synchronize the edit to it.
3. If a suitable text-to-speech tool is actually available in the current environment, generate narration audio using an appropriate voice.
4. If no voice generation capability is available, do not pretend to create a voiceover. Finish the strongest feasible video with timed captions and suitable music/SFX, then state briefly that voiceover was unavailable.

Use only music/SFX that are user-provided, original/generated in the workflow, public-domain, or clearly licensed for the intended use. Keep an audio credit note when required.

### D. Build and render
- Use the available video-production environment and the Kholiq Visual Lab production guidance when that Skill is available.
- Prefer a complete rendered MP4 over merely providing source code.
- Default export: MP4, H.264 video, AAC audio when audio exists, 1080×1920, 30 fps, 9:16.
- Keep project files/source alongside the final render when practical.
- If the environment cannot render video, produce the closest useful editable project/source and state the exact limitation. Never label source code as a finished video.

### E. Quality assurance
Before delivery:
- Confirm the output file exists and can be opened/probed.
- Check duration, resolution, frame rate, and audio stream when applicable.
- Inspect representative frames or a contact sheet for text collisions, clipping, visual glitches, inconsistent characters, empty frames, and safe-area issues.
- Check voiceover/caption timing and sound synchronization.
- Fix clear defects and render again when feasible.

### F. Deliver
Return the final MP4 as a downloadable attachment/link when supported. Include only:
- A short completion statement
- Duration, resolution, and frame rate
- Any important limitation or missing asset (only if applicable)

Do not ask “what next?” or offer extra services after the render. The user invoked an execution command and expects the video.

## Continuity and project-specific context
- Treat user-provided project documents, current conversation facts, and attached assets as authoritative for that project.
- Do not import Republic of Santara facts into unrelated videos.
- For Republic of Santara, preserve the user's established canon and distinguish confirmed facts, citizen aspirations, presidential decisions, and completed results. Never turn an aspiration into a completed build without evidence.
- For other projects, do not assume Santara rules apply.

## Reference
For detailed visual motion, sound design, editing, rendering, and QA standards, read `references/kholiq-visual-lab-production-principles.md`. If the separate **Kholiq Visual Lab** Skill is enabled, use it together with this execution workflow.
