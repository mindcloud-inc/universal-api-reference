# Mark Notification Read with Shuffler

Marks a notification as read in Shuffler.

## Endpoint

- **Method:** `GET`
- **Path:** `/notifications/{notificationId}/markasread`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Mark Notification Read](https://shuffler.io/docs/API#mark-notification-as-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notificationId` | path | `string` | yes | Notification Id path parameter. |
