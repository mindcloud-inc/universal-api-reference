# Get Slack Notification Rule with Rollbar

Retrieves a Slack notification rule from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/notifications/slack/rule/:ruleId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Slack Notification Rule](https://docs.rollbar.com/reference/get_api-1-notifications-slack-rule-rule-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleId` | path | `number` | yes | Notification rule identifier |
