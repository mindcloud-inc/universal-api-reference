# Get Local Variables with Figma

Retrieves local variables from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:file_key/variables/local`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Get Local Variables](https://developers.figma.com/docs/rest-api/variables-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_key` | path | `string` | yes | The Figma file key. |
