# Delete File with Anthropic

Deletes an uploaded file from Anthropic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/files/:file_id`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Delete File](https://platform.claude.com/docs/en/api/beta/files/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | Identifier of the file to delete. |
