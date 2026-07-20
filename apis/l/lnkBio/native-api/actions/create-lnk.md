# Create Lnk with Lnk.Bio

Creates a new Lnk in Lnk.Bio.

## Endpoint

- **Method:** `POST`
- **Path:** `/lnk/add`
- **Base URL:** `https://lnk.bio/oauth/v1`
- **Official documentation:** [Create Lnk](https://api.lnk.bio/api-6746008)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The title shown for the Lnk on your public Lnk.Bio profile. |
| `link` | body | `string` | yes | The destination URL for the new Lnk. |
| `image` | body | `string` | no | Optional image URL for the Lnk. |
| `group_id` | body | `number` | no | Optional Lnk.Bio group identifier for the new Lnk. |
| `schedule_from` | body | `string` | no | Optional RFC3339 timestamp for when the Lnk should become active. |
| `schedule_to` | body | `string` | no | Optional RFC3339 timestamp for when the Lnk should stop being active. |
