# Update Feed with Inoreader

Updates an existing feed subscription in Inoreader.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscription/edit`
- **Base URL:** `https://www.inoreader.com/reader/api/0`
- **Official documentation:** [Update Feed](https://www.inoreader.com/developers/edit-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ac` | body | `string` | yes | Subscription edit action such as unfollow, edit, or subscribe. |
| `s` | body | `string` | yes | Subscription stream ID to update. |
| `t` | body | `string` | no | Optional new subscription title. |
| `a` | body | `string` | no | Optional folder label to add. |
| `r` | body | `string` | no | Optional folder label to remove. |
