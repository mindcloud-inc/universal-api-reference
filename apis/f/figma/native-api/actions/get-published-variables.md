# Get Published Variables with Figma

Retrieves published variables from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:file_key/variables/published`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Get Published Variables](https://developers.figma.com/docs/rest-api/variables-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_key` | path | `string` | yes | The Figma file key. |
