# List Notifications with Strategypoint

Retrieves notifications from Strategypoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/notifications`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [List Notifications](https://developer.clearpointstrategy.com/reference/listadminnotifications-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Maximum number of notifications to return. |
| `object` | query | `string` | no | Filter notifications by related object type. |
| `objectId` | query | `number` | no | Filter notifications by related object identifier. |
| `periodId` | query | `number` | no | Filter notifications by period identifier. |
| `userId` | query | `string` | no | Filter notifications by user identifier. |
