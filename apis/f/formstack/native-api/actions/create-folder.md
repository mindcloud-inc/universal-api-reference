# Create Folder with Formstack

Creates a new folder in Formstack.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Create Folder](https://developers.formstack.com/reference/createfolder-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the folder. |
| `parent` | body | `number` | no | Parent folder ID. |
