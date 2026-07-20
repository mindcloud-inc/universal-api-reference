# Create Folder with Files.com

Creates a new folder in Files.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Create Folder](https://developers.files.com/rest/files/files#create-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | Folder path to create, without leading or trailing slashes. |
| `mkdir_parents` | query | `boolean` | no | Create missing parent folders automatically when true. |
