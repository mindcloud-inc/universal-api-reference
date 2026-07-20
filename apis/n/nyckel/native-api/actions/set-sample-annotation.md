# Set Sample Annotation with Nyckel

Updates a sample annotation in Nyckel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/functions/:functionId/samples/:sampleId/annotation`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `sampleId` | path | `string` | yes | Nyckel sample identifier. |
| `labelId` | body | `string` | no | Label ID to set as the sample annotation. |
| `labelName` | body | `string` | no | Label name to set as the sample annotation. |
