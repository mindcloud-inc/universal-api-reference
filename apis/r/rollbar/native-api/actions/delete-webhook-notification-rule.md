# Delete Webhook Notification Rule with Rollbar

Deletes a webhook notification rule from Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/notifications/webhook/rule/:ruleId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Delete Webhook Notification Rule](https://docs.rollbar.com/reference/delete_api-1-notifications-webhook-rule-rule-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleId` | path | `number` | yes | Notification rule identifier |
