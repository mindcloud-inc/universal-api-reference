# Simulate Webhook with Printify

Simulates a webhook in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/webhooks/:webhook_id/simulate`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Simulate Webhook](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `anything` | body | `string` | no | Arbitrary payload echoed in the simulated webhook resource. |
| `shop_id` | path | `number` | yes | Printify shop id. |
| `webhook_id` | path | `string` | yes | Printify webhook id. |
