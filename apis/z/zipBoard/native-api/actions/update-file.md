# Update File with zipBoard

Updates an existing file in zipBoard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/files/:id`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Update File](https://help.zipboard.co/article/179-api-for-files-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated file description. |
| `id` | path | `string` | yes | File record ID to update. |
| `name` | body | `string` | no | Updated file name. |
| `url` | body | `string` | no | Updated review URL. |
