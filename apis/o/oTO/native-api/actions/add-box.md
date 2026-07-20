# Add Box with OTO

Creates a new box in OTO.

## Endpoint

- **Method:** `POST`
- **Path:** `/addBox`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [Add Box](https://help.tryoto.com/en/support/solutions/articles/150000213809-shipments-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the new box template. |
| `length` | body | `number` | yes | Box length. |
| `width` | body | `number` | yes | Box width. |
| `height` | body | `number` | yes | Box height. |
