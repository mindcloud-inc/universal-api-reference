# Get File Images with Figma

Retrieves image fills from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:key/images`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Get File Images](https://developers.figma.com/docs/rest-api/file-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Key of the file to fetch image fills from. |
