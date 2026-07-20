# Get webhook log with AiWifi

Retrieves details for a webhook delivery log in AiWifi.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/{{brandId}}/webhook-logs/{{logId}}`
- **Base URL:** `https://api.aiwifi.io/api/v1`
- **Official documentation:** [Get webhook log](https://help.aiwifi.io/en/category/webhook/article/logs-validation-and-testing-of-webhooks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `logId` | path | `number` | yes |
