# Get File Metadata with Anthropic

Retrieves metadata for an Anthropic file.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files/:file_id`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Get File Metadata](https://platform.claude.com/docs/en/api/beta/files/retrieve_metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | Identifier of the file to retrieve. |
