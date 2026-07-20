# Extend Card with Writeathon

Creates a child card under a Writeathon card.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{userId}/cards/extend`
- **Base URL:** `https://api.writeathon.cn`
- **Official documentation:** [Extend Card](https://guide.writeathon.cn/help/tools/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | body | `string` | yes | The parent card ID to extend. |
| `title` | body | `string` | no | Optional title for the new extended card. |
| `content` | body | `string` | yes | The content for the new extended card. |
