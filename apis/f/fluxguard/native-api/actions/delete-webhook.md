# Delete Webhook with Fluxguard

Deletes a webhook from Fluxguard.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/account/webhook`
- **Base URL:** `https://api.fluxguard.com`
- **Official documentation:** [Delete Webhook](https://fluxguard.com/how-to-guides/use-our-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Identifier of the webhook to delete. |
