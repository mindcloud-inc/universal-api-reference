# Create Card with Writeathon

Creates a new card in Writeathon.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{userId}/cards`
- **Base URL:** `https://api.writeathon.cn`
- **Official documentation:** [Create Card](https://guide.writeathon.cn/help/tools/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Optional card title. If omitted, Writeathon creates one automatically. |
| `content` | body | `string` | yes | The card content to save in Writeathon. |
| `space` | body | `string` | no | Optional Writeathon space ID. Leave blank to use the default space. |
