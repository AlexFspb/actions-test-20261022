# Personal iPhone build: working agreements

This independent repository belongs to AlexFspb: AlexFspb/actions-test-20261022. It was copied from AlexFspb/3d-model-anything, whose upstream is wesbos/3d-model-anything. Preserve upstream attribution and licenses.

## Resume before working

- Read this file and PLAN.md from the current main branch before work, after context compaction, and when handing work to another chat. Use the GitHub connector explicitly when there is no local checkout; do not assume remote files are automatically loaded.
- PLAN.md is the source of truth for the user's goal, accepted decisions, progress, evidence, blockers, and next action. Update it after each completed milestone or material failure. Preserve the original goal unless the user changes it.
- Distinguish prepared, built, installed, scan-tested, export-tested, and re-sign-tested. Never infer device success from CI success.

## Authorized goal and constraints

- Build this app for the user's own iPhone 16 Pro (reported iOS 26.6.1), install from Windows with a free Apple Account through iloader, verify one room scan, ZIP export, and repeat signing without data loss.
- The user explicitly authorized copying the entire fork into AlexFspb/actions-test-20261022 and creating a local clone on 2026-10-22. Local Git work and GitHub Actions checkout are now allowed. The previous no-local-clone constraint is superseded. Keep this repository as the current working source.
- Use free standard GitHub Actions in this public repository. Do not enable paid services, publish to App Store/TestFlight, change iOS, or switch installation methods without user direction.
- Keep app changes limited to fixes necessary for building and running it. Preserve house-capture/5 and other public formats. Three.js reconstruction and SideStore are deferred.
- Never capture or control the user's screen or application windows without explicit permission. The user authorized browser control for the GitHub setup in this chat; this is not blanket permission for desktop apps or the iPhone. Prefer connectors and APIs.
- The user enters Apple credentials, confirms trust, enables Developer Mode, and performs physical scanning. Never store passwords, certificates, pairing files, device identifiers, or personal scans in the public repository or CI artifacts.

## Build and installation invariants

- Stable bundle ID: io.github.alexfspb.housecapture. Preserve the same Apple Account and final installed bundle ID when re-signing; do not uninstall the app to refresh it.
- CI builds unsigned Release for a physical iPhone (arm64), not a simulator. Device signing happens locally with iloader.
- Keep GitHub Pages deployment disabled for this personal-build repository. The copied Pages workflow must skip repositories other than wesbos/3d-model-anything.
- Save build provenance and SHA-256 with each IPA. Record actual tool versions; hosted runner and Homebrew versions can change, so do not claim bit-for-bit reproducibility.
- Check exported scans against the repository's current format documentation. The user's video transcript is context; it does not override actual file schemas or promise survey-grade accuracy.

## Handoff prompt

Продолжи работу с AlexFspb/actions-test-20261022. Сначала прочитай AGENTS.md и PLAN.md в ветке main, затем продолжай с указанного следующего шага.
