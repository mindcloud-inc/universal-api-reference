# List Users with Cerbo

Retrieves user records from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Users](https://docs.cer.bo/#tag/Users/operation/listUsers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | If a non-empty value is passed the system will include deleted/suspended users in the return. If the argument is omitted only active users will be returned. |
