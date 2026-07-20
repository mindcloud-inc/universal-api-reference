# Extend Card With Attachments with Writeathon

Creates a child card with attachments in Writeathon.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{userId}/cards/extend`
- **Base URL:** `https://api.writeathon.cn`
- **Official documentation:** [Extend Card With Attachments](https://guide.writeathon.cn/help/tools/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | body | `string` | yes | The parent card ID to extend. |
| `title` | body | `string` | no | Optional title for the new extended card. |
| `content` | body | `string` | yes | The content for the new extended card. |
| `attachments` | body | `string` | yes | A JSON-array string of Writeathon attachments. Example: [{"type":"link","title":"Example","url":"https://example.com"}] |
