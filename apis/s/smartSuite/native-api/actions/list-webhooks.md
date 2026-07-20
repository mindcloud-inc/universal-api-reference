# List Webhooks with SmartSuite

Retrieves webhooks from SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `https://webhooks.smartsuite.com/smartsuite.webhooks.engine.Webhooks/ListWebhooks`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [List Webhooks](https://developers.smartsuite.com/docs/solution-data/webhooks/list-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `solution_id` | body | `string` | yes | The SmartSuite solution ID to list webhooks for. |
| `page_size` | body | `number` | no | The number of webhook records to return per page. |
| `page_token` | body | `string` | no | The page token to continue listing webhooks. |
