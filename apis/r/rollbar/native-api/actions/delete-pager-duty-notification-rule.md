# Delete PagerDuty Notification Rule with Rollbar

Deletes a PagerDuty notification rule from Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/notifications/pagerduty/rule/:ruleId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Delete PagerDuty Notification Rule](https://docs.rollbar.com/reference/delete_api-1-notifications-pagerduty-rule-rule-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleId` | path | `number` | yes | Notification rule identifier |
