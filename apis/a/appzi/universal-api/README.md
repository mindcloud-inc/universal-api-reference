# <img src="https://images.mindcloud.co/apps/icons/appzi_1774549365290.png" alt="Appzi logo" width="28" height="28"> Appzi: Universal API

Collect website feedback and user surveys with Appzi portal-based widgets, targeting, and triggers.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/appzi/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.appzi.com
- **Vendor API docs:** https://docs.appzi.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Portal Survey Configurations](actions/list-portal-survey-configurations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appzi/latest/actions/list-portal-survey-configurations?connectionId=$CONNECTION_ID&portalToken=fYbQ6" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Debug Data

| Action | Method | Description |
| --- | --- | --- |
| [Add Debug Metadata](actions/add-debug-metadata.md) | PUT | Generates Appzi debug metadata settings. |

### Feedback Data

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Feedback Data](actions/add-custom-feedback-data.md) | PUT | Generates Appzi custom feedback data settings. |
| [Add Feedback Metadata](actions/add-feedback-metadata.md) | PUT | Generates Appzi feedback metadata settings. |
| [Generate Dynamic Feedback Data](actions/generate-dynamic-feedback-data.md) | POST | Generates Appzi dynamic feedback data settings. |

### Installation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Client Bundle Install Instructions](actions/generate-client-bundle-install-instructions.md) | POST | Generates Appzi client bundle installation instructions. |
| [Generate Client Framework Install Instructions](actions/generate-client-framework-install-instructions.md) | POST | Generates client framework install snippets for Appzi. |
| [Generate JavaScript Loader](actions/generate-java-script-loader.md) | POST | Generates an Appzi JavaScript loader snippet. |
| [Generate One-Line Install Script](actions/generate-one-line-install-script.md) | POST | Generates a one-line Appzi install script. |
| [Generate Settings Object](actions/generate-settings-object.md) | POST | Generates an Appzi settings object snippet. |
| [Generate SSR Install Instructions](actions/generate-ssr-install-instructions.md) | POST | Generates SSR install snippets for Appzi. |

### Installation Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Installation](actions/verify-installation.md) | GET | Retrieves an installation verification checklist from Appzi. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Capture Canvas WebGL Content](actions/capture-canvas-web-gl-content.md) | GET | Retrieves a canvas and WebGL capture snippet from Appzi. |
| [Configure Appzi CSP Headers](actions/configure-appzi-csp-headers.md) | GET | Retrieves CSP header directives from Appzi. |
| [Enable WCAG Mode](actions/enable-wcag-mode.md) | GET | Retrieves Appzi WCAG mode guidance. |
| [Exclude Elements From Screenshots](actions/exclude-elements-from-screenshots.md) | GET | Retrieves a screenshot exclusion snippet from Appzi. |
| [Include Appzi Script Under CSP](actions/include-appzi-script-under-csp.md) | GET | Retrieves Appzi CSP script inclusion guidance. |
| [Prepare CSP-Compatible Appzi Install](actions/prepare-csp-compatible-appzi-install.md) | GET | Retrieves a CSP-safe installation plan from Appzi. |
| [Use Standard Accessibility Mode](actions/use-standard-accessibility-mode.md) | GET | Retrieves Appzi standard accessibility mode guidance. |

### Portal Survey Configuration

| Action | Method | Description |
| --- | --- | --- |
| [List Portal Survey Configurations](actions/list-portal-survey-configurations.md) | GET | Retrieves portal survey configurations from Appzi. |

### Screenshot Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Capture Specific Elements In Screenshots](actions/capture-specific-elements-in-screenshots.md) | GET | Retrieves a screenshot element-capture snippet from Appzi. |
| [Enable Client-Side Screenshot Renderer](actions/enable-client-side-screenshot-renderer.md) | GET | Retrieves a client-side screenshot renderer snippet from Appzi. |
| [Enable Screenshot Debug Mode](actions/enable-screenshot-debug-mode.md) | GET | Retrieves a screenshot debug mode snippet from Appzi. |
| [Use Client-Side Screenshot Renderer](actions/use-client-side-screenshot-renderer.md) | GET | Retrieves Appzi client-side screenshot renderer guidance. |
| [Use Default Screenshot Renderer](actions/use-default-screenshot-renderer.md) | GET | Retrieves Appzi default screenshot renderer guidance. |

### Survey Event

| Action | Method | Description |
| --- | --- | --- |
| [Filter Events By Survey ID](actions/filter-events-by-survey-id.md) | GET | Retrieves a survey event filter snippet from Appzi. |
| [Get Event Object Structure](actions/get-event-object-structure.md) | GET | Retrieves the Appzi survey event object structure. |
| [Listen For Survey Events](actions/listen-for-survey-events.md) | GET | Retrieves a survey event listener snippet from Appzi. |
| [Trigger Function On Survey Open](actions/trigger-function-on-survey-open.md) | POST | Generates an Appzi survey-open handler snippet. |

### Survey Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Open Survey From Ready Callback](actions/open-survey-from-ready-callback.md) | POST | Generates an Appzi ready-callback survey trigger snippet. |
| [Open Survey Inline](actions/open-survey-inline.md) | POST | Generates an inline Appzi survey trigger snippet. |
| [Open Survey On Page Load](actions/open-survey-on-page-load.md) | POST | Generates an Appzi page-load survey trigger snippet. |
| [Open Survey Via HTML Attribute](actions/open-survey-via-html-attribute.md) | POST | Generates an Appzi HTML-attribute survey trigger snippet. |

### Targeting Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Configure Auto-Triggers](actions/configure-auto-triggers.md) | GET | Retrieves Appzi auto-trigger configuration guidance. |
| [Enable Server-Side Trigger Tracking](actions/enable-server-side-trigger-tracking.md) | GET | Retrieves a server-side trigger tracking snippet from Appzi. |
| [Use Custom JavaScript Targeting](actions/use-custom-java-script-targeting.md) | GET | Retrieves a custom JavaScript targeting snippet from Appzi. |
| [Use Default Targeting Rules](actions/use-default-targeting-rules.md) | GET | Retrieves default targeting rules and a snippet from Appzi. |

### User Data

| Action | Method | Description |
| --- | --- | --- |
| [Set Lifecycle Targeting Metadata](actions/set-lifecycle-targeting-metadata.md) | PUT | Generates Appzi lifecycle targeting metadata settings. |
| [Set User Identification](actions/set-user-identification.md) | PUT | Generates an Appzi user identification settings snippet. |
| [Track User Context Data](actions/track-user-context-data.md) | PUT | Generates Appzi user context tracking settings. |

