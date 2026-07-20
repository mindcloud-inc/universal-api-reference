# List Users with Connecteam

Retrieves a list of all users associated with the account. Optionally, filter by user ID to receive specific user information

## Endpoint

- **Method:** `GET`
- **Path:** `/users/v1/users`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [List Users](https://developer.connecteam.com/reference/get_users_users_v1_users_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | — |
| `offset` | query | `number` | no | — |
| `sort` | query | `string` | no | — |
| `order` | query | `string` | no | — |
| `userIds` | query | `array<number>` | no | Send multiple values as a array. |
| `userStatus` | query | `string` | no | — |
| `fullNames` | query | `array<string>` | no | Send multiple values as a array. |
| `phoneNumbers` | query | `array<string>` | no | Send multiple values as a array. |
| `emailAddresses` | query | `array<string>` | no | Send multiple values as a array. |
| `createdAt` | query | `number` | no | — |
| `modifiedAt` | query | `number` | no | — |
| `lastLogin` | query | `number` | no | — |
| `archivedAt` | query | `number` | no | — |
