# Delete Slack Notification Rule with Rollbar

Deletes a Slack notification rule from Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/notifications/slack/rule/:ruleId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Delete Slack Notification Rule](https://docs.rollbar.com/reference/delete_api-1-notifications-slack-rule-rule-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleId` | path | `number` | yes | Notification rule identifier |
