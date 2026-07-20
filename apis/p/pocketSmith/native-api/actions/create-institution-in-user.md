# Create Institution In User with PocketSmith

Creates an institution for a PocketSmith user.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:id/institutions`
- **Base URL:** `https://api.pocketsmith.com/v2`
- **Official documentation:** [Create Institution In User](https://developers.pocketsmith.com/reference/post_users-id-institutions-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency_code` | body | `string` | yes | A currency code for the institution. |
| `id` | path | `number` | yes | The unique identifier of the PocketSmith user. |
| `title` | body | `string` | yes | A title for the institution. |
