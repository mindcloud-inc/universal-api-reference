# Create Webhook with SmartSuite

Creates a new webhook in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `https://webhooks.smartsuite.com/smartsuite.webhooks.engine.Webhooks/CreateWebhook`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Create Webhook](https://developers.smartsuite.com/docs/solution-data/webhooks/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook` | body | `object` | yes | The SmartSuite webhook object to create, including locator, kinds, filter, and notification_status. |
