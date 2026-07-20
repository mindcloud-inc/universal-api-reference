# Create Text Note with Speak Ai

Creates a text note in Speak Ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/text/create`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [Create Text Note](https://docs.speakai.co/#1001bb40-bc9c-42f8-ad2d-03c5cf131cb6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Display name for the text note. |
| `text` | body | `string` | yes | HTML or plain text content to display in the editor. |
| `rawText` | body | `string` | yes | Raw plain-text content that Speak Ai should analyze. |
| `folderId` | body | `string` | no | Optional folder that should contain the text note. |
| `description` | body | `string` | no | Optional description for the text note. |
| `tags[]` | body | `array<string>` | no | Tags to associate with the text note. |
| `remark` | body | `string` | no | Optional remark to store with the text note. |
