# List File Components with Figma

Retrieves components from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:file_key/components`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [List File Components](https://developers.figma.com/docs/rest-api/component-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_key` | path | `string` | yes | Key of the Figma file. |
