# Deployments, at your pace

A quiet guide to eight deployment patterns, with still diagrams, reader-controlled interactive steps, and optional slow videos.

The guide is designed to reduce competing motion without removing engineering detail. Different readers have different preferences; text alternatives remain available.

**Read the article:** <https://sandraahlgrimm.github.io/deployments-at-your-pace/>

**Use the interactive guide:** <https://sandraahlgrimm.github.io/deployments-at-your-pace/interactive.html>

## Reader controls

- The interactive guide always opens paused. Gentle motion is off for new readers; the browser can remember the selected pattern, step, pace, and motion preference.
- Back, Next step, and the four numbered step buttons work without animation. Optional playback advances at 6 or 10 seconds per step and stops at the last step without looping or changing patterns. Pause and Escape stop playback and moving markers.
- The system's reduced-motion preference disables moving markers, even if a motion preference was previously saved. Timed step playback is still a separate, explicit choice.
- The article shows still diagrams first. Its eight silent, one-minute videos have native controls, no autoplay or looping, and `preload="none"`. Only one video can play at a time. Videos pause when out of view, collapsed, the page is hidden, Escape is pressed, or text-only mode is enabled.
- Text-only mode retains the article's explanations and transcript links. Every video has a poster, English VTT and SRT step descriptions, and a plain-text transcript. Each video holds four stages for 15 seconds each.
- Save HTML downloads the self-contained interactive guide. Its manual controls need JavaScript, but no server or external resources; preferences are saved only when browser storage is available.

The interactive motion switch does not control the fixed MP4 videos. Downloaded videos and other hosts have their own playback and autoplay settings. Text, stills, and manual steps remain the no-motion alternatives. These controls are design choices, not a claim of universal neurodivergent accessibility or certified WCAG compliance.

## Static files

| Path | Purpose |
| --- | --- |
| `index.html` | Complete article, stills, optional video players, and text-only controls |
| `interactive.html` | Self-contained diagrams and controls for all eight patterns |
| `article.md` | Markdown version of the article |
| `media-manifest.json` | Public site URL, media paths, alt text, and video metadata |
| `images/` | Cover, eight scene previews, and eight video posters |
| `videos/` | Eight silent H.264 MP4 walkthroughs |
| `captions/`, `transcripts/` | VTT/SRT step descriptions and plain-text alternatives |
| `.nojekyll` | Serve the publishing root as static files without Jekyll processing |

Edit the HTML and Markdown directly; there is no framework, package installation, or build step. Keep corresponding explanations in `index.html`, `article.md`, and `interactive.html` consistent. If media changes, update the matching stills, posters, captions, transcripts, and manifest metadata together.

Keep asset and companion links relative, such as `images/01-rolling.png` and `interactive.html?pattern=rolling`. The site is served below `/deployments-at-your-pace/`, not the domain root. Pattern links select the requested pattern at its first step, paused. Supported IDs are `rolling`, `blue-green`, `canary`, `feature-flag`, `progressive`, `shadow`, `ab`, and `immutable`.

## GitHub Pages publication

In **Settings > Pages**, use **Deploy from a branch**, branch **main**, folder **/ (root)**. Keep `.nojekyll` at that root. Changes merged into `main` trigger GitHub's branch-based Pages deployment; no custom Actions workflow, custom domain, analytics, or third-party scripts are required.

Use a pull request for edits, inspect the diff, and check the Pages build after merging. Verify the public article, companion pattern links, caption tracks, transcripts, and video playback at the project URL above. Publication here does not publish or upload anything to LinkedIn or a separate video host.
