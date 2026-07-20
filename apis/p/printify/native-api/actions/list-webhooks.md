# List Webhooks with Printify

Retrieves webhooks from a Printify shop.

## Endpoint

- **Method:** `GET`
- **Path:** `/shops/:shop_id/webhooks.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [List Webhooks](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_id` | path | `number` | yes | Printify shop id. |
