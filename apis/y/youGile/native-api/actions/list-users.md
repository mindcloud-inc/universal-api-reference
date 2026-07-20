# List users with YouGile

Retrieves a list of users from YouGile.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [List users](https://ru.yougile.com/api-v2#/operations/UserController_search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter users by email address. |
| `projectId` | query | `string` | no | Filter users by project membership. |
