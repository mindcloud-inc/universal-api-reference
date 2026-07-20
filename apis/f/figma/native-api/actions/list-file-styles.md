# List File Styles with Figma

Retrieves styles from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:file_key/styles`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [List File Styles](https://developers.figma.com/docs/rest-api/component-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_key` | path | `string` | yes | Key of the Figma file. |
