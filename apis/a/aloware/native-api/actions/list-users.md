# List Users with Aloware

Retrieves user records from your Aloware account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/webhook/users`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [List Users](https://support.aloware.com/en/articles/9352647-api-documentation-users-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Optional user email to look up a specific user record. |
| `user_id` | query | `string` | no | Optional Aloware user ID to look up a specific user record. |
