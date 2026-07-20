# Configure PagerDuty Notifications with Rollbar

Updates PagerDuty notification settings in Rollbar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/notifications/pagerduty`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Configure PagerDuty Notifications](https://docs.rollbar.com/reference/put_api-1-notifications-pagerduty)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | yes | Enable PagerDuty notifications. |
| `service_key` | body | `string` | yes | PagerDuty service key. |
