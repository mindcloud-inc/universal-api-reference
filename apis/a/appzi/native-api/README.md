# Appzi: Native API Reference

A consolidated summary of Appzi's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://docs.appzi.io/
- **API base URL:** `https://api.appzi.io`

## Authentication

### Portal Token

Authenticate with an Appzi portal token copied from Portal Settings > Installation Code.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.appzi.io/installation/)

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Custom Feedback Data](actions/add-custom-feedback-data.md) | `GET https://docs.appzi.io/integration/add-data/` | [docs](https://docs.appzi.io/integration/add-data/#adding-additional-data-to-feedback) |
| [Add Debug Metadata](actions/add-debug-metadata.md) | `GET https://docs.appzi.io/integration/add-data/` | [docs](https://docs.appzi.io/integration/add-data/#debug-issues) |
| [Add Feedback Metadata](actions/add-feedback-metadata.md) | `GET https://docs.appzi.io/integration/add-data/` | [docs](https://docs.appzi.io/integration/add-data/#adding-additional-data-to-feedback) |
| [Capture Canvas WebGL Content](actions/capture-canvas-web-gl-content.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/screenshots/#canvaswebgl-capture) |
| [Capture Specific Elements In Screenshots](actions/capture-specific-elements-in-screenshots.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/screenshots/#capture-specific-elements) |
| [Configure Appzi CSP Headers](actions/configure-appzi-csp-headers.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/csp/#2-configure-csp-headers) |
| [Configure Auto-Triggers](actions/configure-auto-triggers.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/targeting/#auto-triggers) |
| [Enable Client-Side Screenshot Renderer](actions/enable-client-side-screenshot-renderer.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/screenshots/#enable-the-client-side-renderer) |
| [Enable Screenshot Debug Mode](actions/enable-screenshot-debug-mode.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/screenshots/#debug-mode) |
| [Enable Server-Side Trigger Tracking](actions/enable-server-side-trigger-tracking.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/targeting/#server-side-tracking) |
| [Enable WCAG Mode](actions/enable-wcag-mode.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/accessibility/#enable-wcag-mode) |
| [Exclude Elements From Screenshots](actions/exclude-elements-from-screenshots.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/screenshots/#exclude-elements) |
| [Filter Events By Survey ID](actions/filter-events-by-survey-id.md) | `GET https://docs.appzi.io/integration/events/` | [docs](https://docs.appzi.io/integration/events/#filter-events-by-survey-id) |
| [Generate Client Bundle Install Instructions](actions/generate-client-bundle-install-instructions.md) | `GET https://docs.appzi.io/installation/` | [docs](https://docs.appzi.io/installation/#client-bundles) |
| [Generate Client Framework Install Instructions](actions/generate-client-framework-install-instructions.md) | `GET https://docs.appzi.io/installation/` | [docs](https://docs.appzi.io/installation/#client-side-frameworks) |
| [Generate Dynamic Feedback Data](actions/generate-dynamic-feedback-data.md) | `GET https://docs.appzi.io/integration/add-data/` | [docs](https://docs.appzi.io/integration/add-data/#dynamic-data) |
| [Generate JavaScript Loader](actions/generate-java-script-loader.md) | `GET https://docs.appzi.io/installation/` | [docs](https://docs.appzi.io/installation/#javascript-function) |
| [Generate One-Line Install Script](actions/generate-one-line-install-script.md) | `GET https://docs.appzi.io/installation/` | [docs](https://docs.appzi.io/installation/#one-line-script-tag) |
| [Generate Settings Object](actions/generate-settings-object.md) | `GET https://docs.appzi.io/installation/` | [docs](https://docs.appzi.io/installation/#via-the-settings-object) |
| [Generate SSR Install Instructions](actions/generate-ssr-install-instructions.md) | `GET https://docs.appzi.io/installation/` | [docs](https://docs.appzi.io/installation/#server-side-rendering-ssr) |
| [Get Event Object Structure](actions/get-event-object-structure.md) | `GET https://docs.appzi.io/integration/events/` | [docs](https://docs.appzi.io/integration/events/#event-object-structure) |
| [Include Appzi Script Under CSP](actions/include-appzi-script-under-csp.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/csp/#1-include-the-appzi-script) |
| [List Portal Survey Configurations](actions/list-portal-survey-configurations.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/installation/) |
| [Listen For Survey Events](actions/listen-for-survey-events.md) | `GET https://docs.appzi.io/integration/events/` | [docs](https://docs.appzi.io/integration/events/#basic-event-handling) |
| [Open Survey From Ready Callback](actions/open-survey-from-ready-callback.md) | `GET https://docs.appzi.io/integration/triggering-surveys/` | [docs](https://docs.appzi.io/integration/triggering-surveys/#ready-callback) |
| [Open Survey Inline](actions/open-survey-inline.md) | `GET https://docs.appzi.io/integration/triggering-surveys/` | [docs](https://docs.appzi.io/integration/triggering-surveys/#inline-trigger) |
| [Open Survey On Page Load](actions/open-survey-on-page-load.md) | `GET https://docs.appzi.io/integration/triggering-surveys/` | [docs](https://docs.appzi.io/integration/triggering-surveys/#page-load-trigger) |
| [Open Survey Via HTML Attribute](actions/open-survey-via-html-attribute.md) | `GET https://docs.appzi.io/integration/triggering-surveys/` | [docs](https://docs.appzi.io/integration/triggering-surveys/#html-attribute) |
| [Prepare CSP-Compatible Appzi Install](actions/prepare-csp-compatible-appzi-install.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/csp/#implementation-steps) |
| [Set Lifecycle Targeting Metadata](actions/set-lifecycle-targeting-metadata.md) | `GET https://docs.appzi.io/integration/add-data/` | [docs](https://docs.appzi.io/integration/add-data/#lifecycle-targeting) |
| [Set User Identification](actions/set-user-identification.md) | `GET https://docs.appzi.io/integration/add-data/` | [docs](https://docs.appzi.io/integration/add-data/#user-identification) |
| [Track User Context Data](actions/track-user-context-data.md) | `GET https://docs.appzi.io/integration/add-data/` | [docs](https://docs.appzi.io/integration/add-data/#track-user-context) |
| [Trigger Function On Survey Open](actions/trigger-function-on-survey-open.md) | `GET https://docs.appzi.io/integration/events/` | [docs](https://docs.appzi.io/integration/events/#trigger-a-function-when-survey-opens) |
| [Use Client-Side Screenshot Renderer](actions/use-client-side-screenshot-renderer.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/screenshots/#client-side-renderer) |
| [Use Custom JavaScript Targeting](actions/use-custom-java-script-targeting.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/targeting/#custom-targeting) |
| [Use Default Screenshot Renderer](actions/use-default-screenshot-renderer.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/screenshots/#default-renderer-server) |
| [Use Default Targeting Rules](actions/use-default-targeting-rules.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/targeting/#default-targeting) |
| [Use Standard Accessibility Mode](actions/use-standard-accessibility-mode.md) | `GET /api/probe/:portalToken` | [docs](https://docs.appzi.io/configuration/accessibility/#standard-mode) |
| [Verify Installation](actions/verify-installation.md) | `GET https://docs.appzi.io/installation/` | [docs](https://docs.appzi.io/installation/#verifying-installation) |
