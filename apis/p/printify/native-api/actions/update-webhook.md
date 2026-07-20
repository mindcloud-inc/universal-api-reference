# Update Webhook with Printify

Updates a webhook in Printify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/shops/:shop_id/webhooks/:webhook_id.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Update Webhook](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_id` | path | `number` | yes | Printify shop id. |
| `url` | body | `string` | yes | Updated destination URL for webhook delivery. |
| `webhook_id` | path | `string` | yes | Printify webhook id. |
