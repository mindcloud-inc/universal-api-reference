# Update PagerDuty Notification Rule with Rollbar

Updates a PagerDuty notification rule in Rollbar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/notifications/pagerduty/rule/:ruleId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Update PagerDuty Notification Rule](https://docs.rollbar.com/reference/put_api-1-notifications-pagerduty-rule-rule-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleId` | path | `number` | yes | Notification rule identifier |
