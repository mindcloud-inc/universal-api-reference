# Update User with Documently

Updates an existing user in Documently.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:userId`
- **Base URL:** `https://app.documently.io/api`
- **Official documentation:** [Update User](https://app.documently.io/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | User email address. |
| `firstname` | body | `string` | no | User first name. |
| `lastname` | body | `string` | no | User last name. |
| `userId` | path | `string` | no | Documently user ID. |
