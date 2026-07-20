# Delete Lnk with Lnk.Bio

Deletes an existing Lnk from Lnk.Bio.

## Endpoint

- **Method:** `POST`
- **Path:** `/lnk/delete`
- **Base URL:** `https://lnk.bio/oauth/v1`
- **Official documentation:** [Delete Lnk](https://api.lnk.bio/api-6746009)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `link_id` | body | `number` | yes | The identifier of the Lnk to delete. |
