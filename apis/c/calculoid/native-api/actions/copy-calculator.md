# Copy Calculator with Calculoid

## Endpoint

- **Method:** `GET`
- **Path:** `/calculator/copy/:calculatorId`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [Copy Calculator](https://www.calculoid.com/documentation-new)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calculatorId` | path | `string` | yes | Calculoid calculator ID to copy. |
