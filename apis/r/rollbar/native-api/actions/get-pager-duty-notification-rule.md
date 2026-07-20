# Get PagerDuty Notification Rule with Rollbar

Retrieves a PagerDuty notification rule from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/notifications/pagerduty/rule/:ruleId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get PagerDuty Notification Rule](https://docs.rollbar.com/reference/get_api-1-notifications-pagerduty-rule-rule-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleId` | path | `number` | yes | Notification rule identifier |
