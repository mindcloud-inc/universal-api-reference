# Get Notification with Strategypoint

Retrieves a notification from Strategypoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/notifications/{notificationId}`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [Get Notification](https://developer.clearpointstrategy.com/reference/getnotification-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notificationId` | path | `number` | yes | The unique notification identifier. |
| `object` | query | `string` | no | Resolve the notification in the context of a related object type. |
