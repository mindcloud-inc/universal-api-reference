# Get Tax Return Data with Syntage

Retrieves tax return data from Syntage.

## Endpoint

- **Method:** `GET`
- **Path:** `/tax-returns/:id/data`
- **Base URL:** `https://api.sandbox.syntage.com`
- **Official documentation:** [Get Tax Return Data](https://docs.syntage.com/api-reference/ds-mx-sat-tax-returns/retrieve-a-tax-return-data.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The tax return identifier. |
