# <img src="https://images.mindcloud.co/apps/icons/candu-logo_1781291423751.jpeg" alt="Candu logo" width="28" height="28"> Candu: Universal API

Candu lets teams drive in-app onboarding and product adoption with embeddable content, targeting data, and webhook-based event ingestion.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/candu/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.candu.ai
- **Vendor API docs:** https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Content Metadata](actions/list-content-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/candu/latest/actions/list-content-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Track Checklist Group Complete](actions/track-checklist-group-complete.md) | POST | Tracks a checklist group completion event in Candu. |
| [Track Checklist Item State Updated](actions/track-checklist-item-state-updated.md) | POST | Tracks a checklist item state update event in Candu. |
| [Track Content Dismiss](actions/track-content-dismiss.md) | POST | Tracks a content dismiss event in Candu. |
| [Track Content Interaction](actions/track-content-interaction.md) | POST | Tracks a content interaction event in Candu. |
| [Track Content View](actions/track-content-view.md) | POST | Tracks a content view event in Candu. |
| [Track Event](actions/track-event.md) | POST | Tracks a custom event for a Candu user. |
| [Track Experiment Impression](actions/track-experiment-impression.md) | POST | Tracks an experiment impression event in Candu. |
| [Track Flow Step View](actions/track-flow-step-view.md) | POST | Tracks a flow step view event in Candu. |
| [Track Form Submission](actions/track-form-submission.md) | POST | Tracks a form submission event in Candu. |
| [Track Hotspot Beacon Render](actions/track-hotspot-beacon-render.md) | POST | Tracks a hotspot beacon render event in Candu. |
| [Track Hotspot Dismiss](actions/track-hotspot-dismiss.md) | POST | Tracks a hotspot dismiss event in Candu. |
| [Track Hotspot Group Dismiss](actions/track-hotspot-group-dismiss.md) | POST | Tracks a hotspot group dismiss event in Candu. |
| [Track Hotspot Tooltip Open](actions/track-hotspot-tooltip-open.md) | POST | Tracks a hotspot tooltip open event in Candu. |
| [Track Tour Completion](actions/track-tour-completion.md) | POST | Tracks a tour completion event in Candu. |
| [Track Tour Step Dismiss](actions/track-tour-step-dismiss.md) | POST | Tracks a tour step dismiss event in Candu. |
| [Track Tour Step View](actions/track-tour-step-view.md) | POST | Tracks a tour step view event in Candu. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Associate User With Group](actions/associate-user-with-group.md) | PUT | Associates a user with a group in Candu. |
| [Upsert Group](actions/upsert-group.md) | PUT | Updates a group in Candu, or creates it if needed. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Content Metadata](actions/list-content-metadata.md) | GET | Retrieves content metadata records from Candu. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Identify User](actions/identify-user.md) | PUT | Updates a user profile in Candu. |

