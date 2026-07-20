# List Users with SupportBee

Retrieves users and customer groups from SupportBee.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [List Users](https://supportbee.com/docs/api/reference#tag/Users/paths/~1users/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `with_invited` | query | `boolean` | no | If true, include invited users. |
| `with_roles` | query | `string` | no | Include role information when requested. |
| `type` | query | `string` | no | Filter by user type. |
