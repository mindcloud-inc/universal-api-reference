# Delete Calculator with Calculoid

## Endpoint

- **Method:** `POST`
- **Path:** `/calculator/delete/:calculatorId`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [Delete Calculator](https://www.calculoid.com/documentation-new)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calculatorId` | path | `string` | yes | Calculoid calculator ID to delete. |
