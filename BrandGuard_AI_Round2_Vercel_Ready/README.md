# BrandGuard AI - CodeNova India Round 2 Prototype

A browser-based prototype for the BrandGuard AI pre-publication governance workflow.

## Run it

1. Download or unzip this folder.
2. Open `index.html` in the latest Chrome or Edge browser.
3. Select **Review content**.
4. Click **Load risky example**, then **Run BrandGuard review**.
5. Expand each finding to inspect its rule, evidence, confidence and suggested fix.
6. Apply a fix and run the review again. The app requires a fresh review after edits.
7. Send the item for human review. Open **Approval queue** and record a human decision.
8. Explore **Knowledge vault**, **Governance insights**, **Activity log** and **Settings**.

No Node.js, npm install, API key or server is required for this local demo.

## Round 2 core workflow implemented

- Content submission for social posts, advertisements, email, documents, press releases and product pages.
- Local review of unsupported claims, broad factual statements, tone, preferred terminology and readability.
- Rule IDs, cited knowledge-vault sources, explanations, confidence and suggested corrections.
- Brand risk score and severity indicators.
- Apply-fix actions that edit the draft and require a fresh review.
- Human approval queue with approve, request changes and reject decisions and reviewer comments.
- Editable local knowledge vault for facts, guidelines, claims, terminology and registered assets.
- Optional image upload with registered-filename check and simple sampled brand-colour heuristic.
- Governance insights, activity log, local settings and activity export.
- Responsive layout; no horizontal page overflow at the tested 390px mobile viewport.

## Technology and implementation disclosure

- **Frontend:** Single-file HTML, CSS and vanilla JavaScript.
- **Review engine:** Deterministic, rule-based local demo logic. It is not a connected LLM and does not make external API calls.
- **Knowledge retrieval:** The prototype checks its local approved knowledge entries using browser-side logic. This is a lightweight demonstration, not production vector search/RAG.
- **Visual check:** Browser canvas samples an uploaded image and checks its filename against a demo asset-register pattern. This is not AI logo recognition and cannot prove approval or usage rights.
- **Persistence:** Browser `localStorage` on the current device/browser.
- **Network:** No external API requests from the HTML prototype.

The demo deliberately labels itself **Demo Analysis Mode**. Do not describe the current local rules as a live AI model or production RAG integration.

## Changes from the Round 1 plan

1. Narrowed the implementation to the judging-critical pre-publication workflow rather than spreading effort across a large set of secondary screens.
2. Turned the planned multi-agent/RAG concept into a working local review simulation with transparent rules and evidence references, so the full flow can be demonstrated without an API key or network dependency.
3. Added editable sample knowledge, apply-fix/re-review behaviour and a real human decision queue to demonstrate the loop from content submission through approval.

## Three meaningful Round 3 improvements

1. **Secure multi-organisation backend:** Add authentication, organisation workspaces, role-based access, encrypted server-side knowledge storage and immutable audit history.
2. **Grounded AI + RAG:** Integrate a hosted or private LLM, a vector database and specialist fact/brand/claims agents. Require citations to retrieved approved sources and evaluate precision, recall and reviewer agreement on a test set.
3. **Multimodal governance:** Add OCR and vision-based document/image checks for logo variants, brand colours, typography, layout, alt text and accessibility, with direct integrations into content-publishing workflows.

## Before submitting to CodeNova

This package is a local prototype, **not a public hosted project URL**. The downloaded file link is not suitable as the public project link judges must open in an incognito window. Deploy `index.html` to a public static host (for example, Vercel, Netlify or GitHub Pages), open the deployed URL in a private/incognito window, and confirm that the review and approval flow works without sign-in. Create a public source-code repository and add these files before submitting.
