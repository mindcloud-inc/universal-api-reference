# Delete Email Notification Rule with Rollbar

Deletes an email notification rule from Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/notifications/email/rule/:ruleId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Delete Email Notification Rule](https://docs.rollbar.com/reference/delete_api-1-notifications-email-rule-rule-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleId` | path | `number` | yes | Notification rule identifier |
