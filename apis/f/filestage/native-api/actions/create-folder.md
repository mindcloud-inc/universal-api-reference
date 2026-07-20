# Create Folder with Filestage

Creates a new folder in Filestage.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Create Folder](https://developers.filestage.io/docs/api/km0e5pq67m95m-create-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `parentId` | body | `string` | no |
