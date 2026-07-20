# Create Webhook with Printify

Creates a webhook in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/webhooks.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Create Webhook](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_id` | path | `number` | yes | Printify shop id. |
| `topic` | body | `string` | yes | Webhook event topic. |
| `url` | body | `string` | yes | Destination URL for webhook delivery. |
