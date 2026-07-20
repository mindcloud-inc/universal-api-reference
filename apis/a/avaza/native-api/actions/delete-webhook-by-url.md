# Delete Webhook By URL with Avaza

Deletes a webhook from Avaza by callback URL.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/Webhook`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Delete Webhook By URL](https://api.avaza.com/#!/Webhook/Webhook_DeleteByUrl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | query | `string` | yes | Target URL that should be used to delete subscriptions |
