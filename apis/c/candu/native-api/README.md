# Candu: Native API Reference

A consolidated summary of Candu's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api
- **API base URL:** `https://api.candu.ai/api`

## Authentication

### API Key

Authenticate to Candu with a workspace API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `content-type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Associate User With Group](actions/associate-user-with-group.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api) |
| [Identify User](actions/identify-user.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api) |
| [List Content Metadata](actions/list-content-metadata.md) | `GET /contentMetadata` | [docs](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api) |
| [Track Checklist Group Complete](actions/track-checklist-group-complete.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Checklist Item State Updated](actions/track-checklist-item-state-updated.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Content Dismiss](actions/track-content-dismiss.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Content Interaction](actions/track-content-interaction.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Content View](actions/track-content-view.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Event](actions/track-event.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api) |
| [Track Experiment Impression](actions/track-experiment-impression.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Flow Step View](actions/track-flow-step-view.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Form Submission](actions/track-form-submission.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Hotspot Beacon Render](actions/track-hotspot-beacon-render.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Hotspot Dismiss](actions/track-hotspot-dismiss.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Hotspot Group Dismiss](actions/track-hotspot-group-dismiss.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Hotspot Tooltip Open](actions/track-hotspot-tooltip-open.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Tour Completion](actions/track-tour-completion.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Tour Step Dismiss](actions/track-tour-step-dismiss.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Track Tour Step View](actions/track-tour-step-view.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/eventing-schema) |
| [Upsert Group](actions/upsert-group.md) | `POST /eventWebhook` | [docs](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api) |
