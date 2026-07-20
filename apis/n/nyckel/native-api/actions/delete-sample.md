# Delete Sample with Nyckel

Deletes an existing sample from Nyckel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/functions/:functionId/samples/:sampleId`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `sampleId` | path | `string` | yes | Nyckel sample identifier. |
