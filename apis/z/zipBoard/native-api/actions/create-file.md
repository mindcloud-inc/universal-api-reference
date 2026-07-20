# Create File with zipBoard

Creates a new file in zipBoard.

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Create File](https://help.zipboard.co/article/179-api-for-files-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional file description. |
| `name` | body | `string` | yes | File display name. |
| `projectid` | body | `string` | yes | Project ID where the file should be stored. |
| `url` | body | `string` | yes | URL of the file to review. |
