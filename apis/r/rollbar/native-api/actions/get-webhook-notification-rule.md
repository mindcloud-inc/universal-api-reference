# Get Webhook Notification Rule with Rollbar

Retrieves a webhook notification rule from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/notifications/webhook/rule/:ruleId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Webhook Notification Rule](https://docs.rollbar.com/reference/get_api-1-notifications-webhook-rule-rule-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleId` | path | `number` | yes | Notification rule identifier |
