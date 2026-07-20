# Update Table with Calculoid

## Endpoint

- **Method:** `POST`
- **Path:** `/calculator/:calculatorId/tables/:tableId/edit`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [Update Table](https://www.calculoid.com/documentation-new)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calculatorId` | path | `string` | yes | Calculoid calculator ID. |
| `tableId` | path | `string` | yes | Calculoid table ID. |
| `name` | body | `string` | yes | Updated table name. |
| `data` | body | `string` | yes | Updated table CSV data or structured data payload. |
