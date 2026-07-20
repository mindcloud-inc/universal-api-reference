# List Samples with Nyckel

Retrieves samples from Nyckel.

## Endpoint

- **Method:** `GET`
- **Path:** `/functions/:functionId/samples`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `count` | query | `number` | no | Maximum number of samples to return. |
| `startIndex` | query | `number` | no | Zero-based sample offset for pagination. |
| `externalId` | query | `string` | no | Filter samples by external ID. |
| `annotated` | query | `boolean` | no | Filter samples that have annotations. |
| `predicted` | query | `boolean` | no | Filter samples that have predictions. |
| `sortBy` | query | `string` | no | Sort field. |
| `sortOrder` | query | `string` | no | Sort direction. |
