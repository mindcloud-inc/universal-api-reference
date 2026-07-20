# <img src="https://images.mindcloud.co/apps/icons/apple-icon_1774979024045.png" alt="Presenton logo" width="28" height="28"> Presenton: Universal API

Presenton is an AI presentation generation platform and API for creating, exporting, editing, and managing presentations, templates, images, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/presenton/latest
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://presenton.ai
- **Vendor API docs:** https://docs.presenton.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Export Presentation](actions/export-presentation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/export-presentation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Async Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Presentation From JSON Async](actions/create-presentation-from-json-async.md) | POST |  |
| [Create Presentation From JSON Async V3](actions/create-presentation-from-json-async-v3.md) | POST |  |
| [Generate Presentation Async](actions/generate-presentation-async.md) | POST |  |
| [Generate Presentation Async V3](actions/generate-presentation-async-v3.md) | POST |  |
| [Get Async Presentation Generation Status](actions/get-async-presentation-generation-status.md) | GET |  |
| [Get Async Task Status V3](actions/get-async-task-status-v3.md) | GET |  |

### Credit Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Info](actions/get-credit-info.md) | GET |  |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [List Uploaded Images](actions/list-uploaded-images.md) | GET |  |
| [List Uploaded Images V3](actions/list-uploaded-images-v3.md) | GET |  |

### Presentation

| Action | Method | Description |
| --- | --- | --- |
| [Create Presentation From JSON](actions/create-presentation-from-json.md) | POST |  |
| [Create Presentation From JSON V3](actions/create-presentation-from-json-v3.md) | POST |  |
| [Delete Presentation](actions/delete-presentation.md) | DELETE |  |
| [Derive Presentation](actions/derive-presentation.md) | POST |  |
| [Edit Presentation](actions/edit-presentation.md) | PUT |  |
| [Generate Presentation](actions/generate-presentation.md) | POST |  |
| [Generate Presentation V3](actions/generate-presentation-v3.md) | POST |  |
| [Get Presentation](actions/get-presentation.md) | GET |  |
| [Get Presentation Editor View](actions/get-presentation-editor-view.md) | GET |  |
| [List Presentations](actions/list-presentations.md) | GET |  |
| [List Presentations V3](actions/list-presentations-v3.md) | GET |  |
| [List Presentations V3 Editor View](actions/list-presentations-v3-editor-view.md) | GET |  |

### Presentation Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Presentation](actions/export-presentation.md) | GET |  |
| [Export Presentation V3](actions/export-presentation-v3.md) | GET |  |

### Presentation Outline

| Action | Method | Description |
| --- | --- | --- |
| [Generate Presentation Outlines V3](actions/generate-presentation-outlines-v3.md) | POST |  |

### Smart Design

| Action | Method | Description |
| --- | --- | --- |
| [List Smart Designs](actions/list-smart-designs.md) | GET |  |

### Standard Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Standard Template](actions/get-standard-template.md) | GET |  |
| [Get Standard Template Example](actions/get-standard-template-example.md) | GET |  |
| [List Standard Templates](actions/list-standard-templates.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET |  |
| [Get Template Example](actions/get-template-example.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Subscriptions V3](actions/list-webhook-subscriptions-v3.md) | GET |  |
| [Subscribe to Webhook](actions/subscribe-to-webhook.md) | POST |  |
| [Subscribe to Webhook V3](actions/subscribe-to-webhook-v3.md) | POST |  |
| [Unsubscribe All Webhook Subscriptions V3](actions/unsubscribe-all-webhook-subscriptions-v3.md) | DELETE |  |
| [Unsubscribe from Webhook](actions/unsubscribe-from-webhook.md) | DELETE |  |
| [Unsubscribe from Webhook V3](actions/unsubscribe-from-webhook-v3.md) | DELETE |  |

