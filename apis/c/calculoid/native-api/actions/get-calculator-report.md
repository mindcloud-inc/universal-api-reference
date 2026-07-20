# Get Calculator Report with Calculoid

## Endpoint

- **Method:** `GET`
- **Path:** `/calculator/report/:calculatorId/:tab`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [Get Calculator Report](https://www.calculoid.com/documentation-new)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calculatorId` | path | `string` | yes | Calculoid calculator ID. |
| `tab` | path | `string` | yes | Report tab to load. Calculoid's app bundle requests calculator reports as /calculator/report/{calculatorId}/{tab}; use view for the default views report. |
