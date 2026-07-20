# Retrieve User with Notion

Retrieves a user from the connected Notion workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Retrieve User](https://developers.notion.com/reference/get-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | Identifier of the user to retrieve. |
