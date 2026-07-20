# Rate Calculator with Calculoid

## Endpoint

- **Method:** `POST`
- **Path:** `/calculator/rate/:calculatorId`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [Rate Calculator](https://www.calculoid.com/documentation-new)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calculatorId` | path | `string` | yes | Calculoid calculator ID. |
| `rating` | body | `number` | yes | Numeric calculator rating. |
