# Create Or Update User with Userflow

Creates or updates a user in Userflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [Create Or Update User](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Unique identifier for the user. |
| `attributes` | body | `object` | no | User attributes to merge into the Userflow user. |
