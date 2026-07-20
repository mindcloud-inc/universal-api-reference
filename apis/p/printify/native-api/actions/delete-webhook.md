# Delete Webhook with Printify

Deletes a webhook from Printify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/shops/:shop_id/webhooks/:webhook_id.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Delete Webhook](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host` | query | `string` | yes | Expected host of the webhook URL. |
| `shop_id` | path | `number` | yes | Printify shop id. |
| `webhook_id` | path | `string` | yes | Printify webhook id. |
