# Delete Webhook with Polaria

Deletes a webhook from Polaria.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/widgets/[:api_key]/webhooks/[:id]`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Delete Webhook](https://help.polaria.ai/hc/rest-api-webhooks/del-widgets-api_key-webhooks-id-delete-a-webhook-2?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_key` | path | `string` | yes | The Polaria widget API key for the target brand. |
| `id` | path | `string` | yes | The ID of the webhook to delete. |
