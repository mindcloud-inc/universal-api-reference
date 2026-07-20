# Get Subscriber Activity with MailerLite

Retrieves activity for a subscriber in MailerLite.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:id/activity-log`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Get Subscriber Activity](https://developers.mailerlite.com/docs/subscribers#fetch-subscriber-activity)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Subscriber ID for the account. |
| `filter[log_name]` | query | `string` | no | Activity log type to include. |
