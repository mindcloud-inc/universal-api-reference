# Configure Slack Notifications with Rollbar

Updates Slack notification settings in Rollbar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/notifications/slack`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Configure Slack Notifications](https://docs.rollbar.com/reference/put_api-1-notifications-slack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `string` | yes | Default Slack channel. |
| `enabled` | body | `boolean` | yes | Enable Slack notifications. |
| `service_account_id` | body | `string` | yes | Slack service account id. |
