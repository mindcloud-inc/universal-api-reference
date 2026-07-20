# Create Folder with Skyvern

Creates a new workflow folder in Skyvern.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/folders`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Create Folder](https://www.skyvern.com/docs/api-reference/workflows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Folder description |
| `title` | body | `string` | yes | Folder title |
