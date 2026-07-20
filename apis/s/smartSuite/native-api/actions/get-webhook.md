# Get Webhook with SmartSuite

Retrieves a webhook from SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `https://webhooks.smartsuite.com/smartsuite.webhooks.engine.Webhooks/GetWebhook`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Get Webhook](https://developers.smartsuite.com/docs/solution-data/webhooks/get-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | body | `string` | yes | The SmartSuite webhook ID to fetch. |
