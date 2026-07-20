# Get Style with Figma

Retrieves a style from Figma by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/styles/:key`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Get Style](https://developers.figma.com/docs/rest-api/component-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | The unique key of the style. |
