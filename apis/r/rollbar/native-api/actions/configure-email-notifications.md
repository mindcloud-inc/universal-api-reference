# Configure Email Notifications with Rollbar

Updates email notification settings in Rollbar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/notifications/email`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Configure Email Notifications](https://docs.rollbar.com/reference/put_api-1-notifications-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | yes | Enable email notifications. |
