# <img src="https://images.mindcloud.co/apps/icons/exa_1774455320114.png" alt="Exa logo" width="28" height="28"> Exa: Universal API

Exa: Search, research, and extract structured web data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/exa/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://exa.ai
- **Vendor API docs:** https://exa.ai/docs/reference/search-api-guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search](actions/search.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/search?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Answer

| Action | Method | Description |
| --- | --- | --- |
| [Answer](actions/answer.md) | GET | Retrieves an answer from Exa. |

### Content Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Contents](actions/get-contents.md) | GET | Retrieves page contents from Exa. |

### Context Response

| Action | Method | Description |
| --- | --- | --- |
| [Context](actions/context.md) | GET | Retrieves context from Exa. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Exa. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Exa. |

### Import

| Action | Method | Description |
| --- | --- | --- |
| [Create Import](actions/create-import.md) | POST | Creates a new import in Exa. |
| [Get Import](actions/get-import.md) | GET | Retrieves an import from Exa. |
| [List Imports](actions/list-imports.md) | GET | Retrieves imports from Exa. |

### Monitor

| Action | Method | Description |
| --- | --- | --- |
| [Create Monitor](actions/create-monitor.md) | POST | Creates a new monitor in Exa. |
| [Delete Monitor](actions/delete-monitor.md) | DELETE | Deletes an existing monitor from Exa. |
| [Get Monitor](actions/get-monitor.md) | GET | Retrieves a monitor from Exa. |
| [List Monitors](actions/list-monitors.md) | GET | Retrieves monitors from Exa. |
| [Trigger Monitor Run](actions/trigger-monitor-run.md) | PUT | Triggers a monitor run in Exa. |
| [Update Monitor](actions/update-monitor.md) | PUT | Updates an existing monitor in Exa. |

### Monitor Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Monitor Run](actions/get-monitor-run.md) | GET | Retrieves a monitor run from Exa. |
| [List Monitor Runs](actions/list-monitor-runs.md) | GET | Retrieves monitor runs from Exa. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds relevant search results in Exa. |

### Similar Link

| Action | Method | Description |
| --- | --- | --- |
| [Find Similar Links](actions/find-similar-links.md) | GET | Finds links similar to a URL in Exa. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Exa. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Exa. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Exa. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Exa. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Exa. |

### Webset

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Webset](actions/cancel-webset.md) | PUT | Cancels a running webset in Exa. |
| [Create Webset](actions/create-webset.md) | POST | Creates a new webset in Exa. |
| [Delete Webset](actions/delete-webset.md) | DELETE | Deletes an existing webset from Exa. |
| [Get Webset](actions/get-webset.md) | GET | Retrieves a webset from Exa. |
| [List Websets](actions/list-websets.md) | GET | Retrieves websets from Exa. |
| [Update Webset](actions/update-webset.md) | PUT | Updates an existing webset in Exa. |

### Webset Enrichment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Webset Enrichment](actions/cancel-webset-enrichment.md) | PUT | Cancels a running webset enrichment in Exa. |
| [Create Webset Enrichment](actions/create-webset-enrichment.md) | POST | Creates a new webset enrichment in Exa. |
| [Delete Webset Enrichment](actions/delete-webset-enrichment.md) | DELETE | Deletes an existing webset enrichment from Exa. |
| [Get Webset Enrichment](actions/get-webset-enrichment.md) | GET | Retrieves a webset enrichment from Exa. |
| [Update Webset Enrichment](actions/update-webset-enrichment.md) | PUT | Updates an existing webset enrichment in Exa. |

### Webset Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Webset Item](actions/get-webset-item.md) | GET | Retrieves a webset item from Exa. |
| [List Webset Items](actions/list-webset-items.md) | GET | Retrieves webset items from Exa. |

### Webset Preview

| Action | Method | Description |
| --- | --- | --- |
| [Preview Webset](actions/preview-webset.md) | GET | Retrieves a webset preview from Exa. |

### Webset Search

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Webset Search](actions/cancel-webset-search.md) | PUT | Cancels a running webset search in Exa. |
| [Create Webset Search](actions/create-webset-search.md) | POST | Creates a new webset search in Exa. |
| [Get Webset Search](actions/get-webset-search.md) | GET | Retrieves a webset search from Exa. |

