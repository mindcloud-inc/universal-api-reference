# Append Card with Writeathon

Appends content to an existing Writeathon card.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{userId}/cards`
- **Base URL:** `https://api.writeathon.cn`
- **Official documentation:** [Append Card](https://guide.writeathon.cn/help/tools/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The existing card title to append content to. |
| `content` | body | `string` | yes | The content to append to the named card. |
| `space` | body | `string` | no | Optional Writeathon space ID. Leave blank to use the default space. |
