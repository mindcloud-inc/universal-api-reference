# Delete Webhook with UniOne

Deletes a webhook from UniOne by URL.

## Endpoint

- **Method:** `POST`
- **Path:** `webhook/delete.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Delete Webhook](https://docs.unione.io/en/web-api-ref#webhook-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook URL to delete. |
