# Update Box with OTO

Updates an existing box in OTO.

## Endpoint

- **Method:** `POST`
- **Path:** `/updateBox`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [Update Box](https://help.tryoto.com/en/support/solutions/articles/150000213809-shipments-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Existing box name to update. |
| `length` | body | `number` | yes | Updated box length. |
| `width` | body | `number` | yes | Updated box width. |
| `height` | body | `number` | yes | Updated box height. |
