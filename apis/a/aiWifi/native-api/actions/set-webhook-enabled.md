# Set webhook enabled with AiWifi

Updates whether a webhook is active in AiWifi.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/brands/{{brandId}}/enable/webhook/{{webhookId}}`
- **Base URL:** `https://api.aiwifi.io/api/v1`
- **Official documentation:** [Set webhook enabled](https://help.aiwifi.io/en/category/webhook/article/webhook-setup-and-configuration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhookId` | path | `number` | yes |
| `enabled` | body | `boolean` | yes |
