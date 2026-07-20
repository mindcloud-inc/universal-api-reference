# Create Table with Calculoid

## Endpoint

- **Method:** `POST`
- **Path:** `/calculator/:calculatorId/tables/create`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [Create Table](https://www.calculoid.com/documentation-new)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calculatorId` | path | `string` | yes | Calculoid calculator ID. |
| `name` | body | `string` | yes | Table name. |
| `data` | body | `string` | yes | Table CSV data or structured data payload. |
