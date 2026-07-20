# Upload File with Anthropic

Uploads a new file to Anthropic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Upload File](https://platform.claude.com/docs/en/api/beta/files/upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | The file to upload. |
