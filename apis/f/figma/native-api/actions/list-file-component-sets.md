# List File Component Sets with Figma

Retrieves component sets from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:file_key/component_sets`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [List File Component Sets](https://developers.figma.com/docs/rest-api/component-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_key` | path | `string` | yes | Key of the Figma file. |
