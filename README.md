# BHG Brand Assets (public CDN)

Public brand assets for Breakwater Hospitality Group email signatures and embeds. Public on purpose: these are only assets meant to render in outbound email (logos already public on our sites). No secrets, ever.

Served to email via `https://raw.githubusercontent.com/BW-BIOS/bhg-brand-assets/main/<path>` (Gmail proxies and caches it).

## What's here
- `breakwater-logo-black.png` and `logos/breakwaterhg.png` - the parent Breakwater wordmark used in signatures.
- `logos/{slug}.png` - one logo per venue domain (wharfftl, regattagrove, johnmartins, pier5). Cached on first use.
- `signature-template.html` - the canonical email-signature template (mirror of the vault copy at Owner/Departments/ai-technology/agents/it-access-desk/signature-template.html).

## How the signature module uses this
Skip (the IT & Access Desk agent) picks a venue by the new hire's email domain (map: `signature-domains.yaml` in the vault), renders `signature-template.html`, and applies it to the mailbox via the Gmail settings API. When a venue logo is not yet here, Skip grabs it (venue brand folder or site) and commits it to `logos/{slug}.png` before rendering. Full step: the `signature-provisioning` runbook in the vault.

Logo convention: target width 200px in the signature; keep source PNGs reasonably sized.
