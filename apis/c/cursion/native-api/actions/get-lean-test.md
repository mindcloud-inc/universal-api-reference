# Get Lean Test with Cursion

Retrieves abbreviated test details from Cursion.

## Endpoint

- **Method:** `GET`
- **Path:** `/test/{{testId}}/lean`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [Get Lean Test](https://docs.cursion.dev/api/test)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `testId` | path | `string` | yes | The test identifier. |
