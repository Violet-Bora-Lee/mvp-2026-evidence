# Microsoft GitHub — Public Issue Reports

**Author:** Bora Lee ([Violet-Bora-Lee](https://github.com/Violet-Bora-Lee))
**Contribution period:** 1 April 2025 – 31 March 2026

---

## Summary

| Repository | Issue # | Status | Outcome |
|-----------|--------:|--------|---------|
| microsoft/vscode-ai-toolkit | [#344](https://github.com/microsoft/vscode-ai-toolkit/issues/344) | Closed | **Fix shipped in pre-release 0.31.2026021209** |
| microsoft/vscode | [#289300](https://github.com/microsoft/vscode/issues/289300) | Closed | Triaged |
| Azure-Samples/mcp-container-ts | [#12](https://github.com/Azure-Samples/mcp-container-ts/issues/12) | Closed | README updated |

---

## 1. microsoft/vscode-ai-toolkit#344 — UX bug shipped to release

**Issue:** <https://github.com/microsoft/vscode-ai-toolkit/issues/344>
**Title:** "Tooltip text is cut off for Top P parameter in Playground"
**Reported:** 2026-02-02
**Closed:** 2026-02-24

### Bug summary
In the AI Toolkit Playground's "Inference parameters" section, the tooltip for the **Temperature** and **Top P** parameters was cut off at the bottom-right corner of the screen, making the parameter explanation unreadable when users selected a model (e.g., gpt-4o via Microsoft Foundry).

### Submission quality
The report included:
- 5-step reproduction
- Expected vs. actual behavior
- Screenshots of the clipped tooltip
- Environment info (VS Code Insider build, AI Toolkit version, macOS)
- A suggested fix using viewport-aware tooltip positioning

### Microsoft engineering response
On 2026-02-24, Microsoft engineering ([@QinghuiMeng-M](https://github.com/QinghuiMeng-M)) confirmed:

> "Thanks for the feedback. Now the bug fix has been merged and will be included in later release of AI Toolkit"
>
> "this bug is fixed in pre-release 0.31.2026021209"

### Impact
End-to-end loop completed in ~3 weeks (report → triage → merge → release). Fix benefits all AI Toolkit Playground users globally.

**Repository:** <https://github.com/microsoft/vscode-ai-toolkit>
**Marketplace:** <https://marketplace.visualstudio.com/items?itemName=ms-windows-ai-studio.windows-ai-studio>

---

## 2. microsoft/vscode#289300 — Chat readiness regression report

**Issue:** <https://github.com/microsoft/vscode/issues/289300>
**Title:** "Chat took too long to get ready"
**Reported:** 2026-01-21
**Closed:** 2026-01-22 (with `info-needed`, `triage-needed` labels)

### Bug summary
On VS Code Insiders 1.109.0-insider (Universal) on Apple Silicon (Apple M1 Max, Darwin 24.5.0), the GitHub Copilot Chat extension version 0.37.2026012003 took unusually long to become ready, blocking productive use.

### Submission quality
- Full system diagnostic dump (CPU, GPU, OS)
- Extension versions
- Reproduction context
- Surfaced during real-world Korean enterprise field testing

**Repository:** <https://github.com/microsoft/vscode>

---

## 3. Azure-Samples/mcp-container-ts#12 — Doc fix for Codespaces auth flow

**Issue:** <https://github.com/Azure-Samples/mcp-container-ts/issues/12>
**Title:** "Broken link" (Codespaces authentication redirect)
**Reported:** 2025-06-23
**Closed:** 2025-07-08

### Bug summary
When deploying the MCP container template inside GitHub Codespaces, `azd auth login` attempts to open a browser for authentication and redirects to localhost — which doesn't work properly in the Codespaces web environment.

### Outcome
Microsoft engineering ([@pamelafox](https://github.com/pamelafox)) added the standard pattern to the README:

> "For GitHub Codespaces users, if the previous command fails, try: `azd auth login --use-device-code`"

### Discovery context
Discovered while running enterprise Korean Codespaces MCP onboarding sessions. The fix follows a standard pattern across many Azure-Samples repos.

**Repository:** <https://github.com/Azure-Samples/mcp-container-ts>

---

## Verification

All three issues are public on Microsoft GitHub organizations and viewable without login.
