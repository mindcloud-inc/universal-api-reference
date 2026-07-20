# List Fields with Nyckel

Retrieves fields from Nyckel.

## Endpoint

- **Method:** `GET`
- **Path:** `/functions/:functionId/fields`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `count` | query | `number` | no | Maximum number of fields to return. |
| `startIndex` | query | `number` | no | Zero-based field offset for pagination. |
