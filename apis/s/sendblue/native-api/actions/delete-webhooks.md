# Delete Webhooks with Sendblue

Deletes webhooks from Sendblue.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/account/webhooks`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Delete Webhooks](https://docs.sendblue.com/api/resources/webhooks/methods/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhooks[]` | body | `array<string>` | yes | Webhook URLs to delete. Send multiple values as a array. |
| `type` | body | `string` | no | The webhook event type to delete from. |
