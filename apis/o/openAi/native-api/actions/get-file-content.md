# Get File Content with Open AI

Retrieves file contents from Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/files/:file_id/content`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Get File Content](https://developers.openai.com/api/reference/files/retrieve-contents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | OpenAI file ID whose content to download. |
