# Update Text Note with Speak Ai

Updates an existing text note in Speak Ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/text/update/:mediaId`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [Update Text Note](https://docs.speakai.co/#dd13ff94-db3b-47b3-9120-51f9929abc5e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaId` | path | `string` | yes | Speak Ai text note media identifier. |
| `name` | body | `string` | no | Updated text note name. |
| `description` | body | `string` | no | Updated text note description. |
| `tags[]` | body | `array<string>` | no | Updated list of tags for the text note. |
| `text` | body | `string` | no | Updated HTML or plain text content. |
| `rawText` | body | `string` | no | Updated raw plain-text content. |
| `remark` | body | `string` | no | Updated remark for the text note. |
