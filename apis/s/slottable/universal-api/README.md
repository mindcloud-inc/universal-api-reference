# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-04-02-at-13_1775145695926.png" alt="Slottable logo" width="28" height="28"> Slottable: Universal API

Slottable integration app for accessing provider APIs with API tokens generated from Slottable integrations settings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/slottable/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://slottable.com/
- **Vendor API docs:** https://slottable.app/docs/p/integrations-and-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Token Details](actions/get-token-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slottable/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Details](actions/get-token-details.md) | GET | Retrieves API token details from Slottable. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Slottable. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Slottable. |

