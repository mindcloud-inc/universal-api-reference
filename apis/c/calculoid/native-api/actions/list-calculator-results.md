# List Calculator Results with Calculoid

## Endpoint

- **Method:** `GET`
- **Path:** `/results/:calculatorId`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [List Calculator Results](https://www.calculoid.com/documentation-new)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calculatorId` | path | `string` | yes | Calculoid calculator ID. |
