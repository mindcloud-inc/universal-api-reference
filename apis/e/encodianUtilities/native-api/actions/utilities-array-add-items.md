# Utilities - Array Add Items with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ArrayAddItems`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Array Add Items](https://support.encodian.com/hc/en-gb/articles/10565757970332)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | The JSON array or object to modify |
| `items` | body | `string` | yes | The items to add to the 'Data' provided |
| `itemPosition` | body | `string` | yes | Set whether to return the first item, last item or a specified item Accepted values: `0`, `1`, `2`. |
| `itemIndex` | body | `number` | no | Index of the item to return. This is only applicable when the 'Item Position' property is set to 'Specific' |
| `path` | body | `string` | no | Select a specific node within the 'Data' using a JSONPath expression |
