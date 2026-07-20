# Get Table with Calculoid

## Endpoint

- **Method:** `GET`
- **Path:** `/calculator/:calculatorId/tables/:tableId`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [Get Table](https://www.calculoid.com/documentation-new)

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
