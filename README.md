# Maestro Story Coach

AI Maestro: Story-to-Symphony. Students pick a beat (Setup, Tension, Turn, Resolution), tap **SAY IT** to talk their 5 sentences, and get one strength plus one question from the coach. The coach never rewrites their story.

- `index.html` – the page (one-tap microphone uses the browser's speech recognition; works in Microsoft Edge and Google Chrome)
- `api/feedback.js` – Vercel function that sends the beat to Claude

## Vercel settings

Project > Settings > Environment Variables:

| Name | Value |
|---|---|
| `ANTHROPIC_API_KEY` | your key from console.anthropic.com (required) |
| `CLASS_CODE` | a short word students type once, e.g. `maestro` (optional, recommended so strangers can't use your key) |
| `MODEL` | optional, defaults to `claude-sonnet-5-5` |

Redeploy after adding or changing a variable.

## Privacy

Spoken words are turned into text by the browser's speech service (Microsoft for Edge, Google for Chrome). Story text and photos go to the Claude API to make feedback. Drafts are saved only in that laptop's browser. Students should use their hero's name, not their own.
