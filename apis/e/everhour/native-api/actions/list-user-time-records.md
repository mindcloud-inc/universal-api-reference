# List User Time Records with Everhour

Retrieves time records for a user from Everhour.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userId/time`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [List User Time Records](https://everhour.docs.apiary.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start date for the time range. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `page` | query | `number` | no | Page number to return. |
| `to` | query | `string` | no | End date for the time range. |
| `userId` | path | `string` | yes | Everhour user ID. |
