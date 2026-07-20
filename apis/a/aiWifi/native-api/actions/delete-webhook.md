# Delete webhook with AiWifi

Deletes an existing webhook configuration from AiWifi.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/brands/{{brandId}}/webhook-configs/{{webhookId}}`
- **Base URL:** `https://api.aiwifi.io/api/v1`
- **Official documentation:** [Delete webhook](https://help.aiwifi.io/en/category/webhook/article/webhook-setup-and-configuration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhookId` | path | `number` | yes |
