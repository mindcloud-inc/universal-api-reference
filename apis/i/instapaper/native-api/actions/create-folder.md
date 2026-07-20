# Create Folder with Instapaper

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1/folders/add`
- **Base URL:** `https://www.instapaper.com`
- **Official documentation:** [Create Folder](https://www.instapaper.com/developers/v1/full-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The folder title. It must be unique for the user. |
