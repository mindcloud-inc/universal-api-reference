# Download File with Anthropic

Downloads content for an Anthropic file.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files/:file_id/content`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Download File](https://platform.claude.com/docs/en/api/beta/files/download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | Identifier of the file to download. |
