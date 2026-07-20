# Upload File Content with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/file/{fileId}/upload`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Upload File Content](https://chatbotkit.com/manuals/files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | The ID of the file to upload |
| `file` | body | `file` | yes | The file to upload |
