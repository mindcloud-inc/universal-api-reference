# List Labels with Nyckel

Retrieves labels from Nyckel.

## Endpoint

- **Method:** `GET`
- **Path:** `/functions/:functionId/labels`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `count` | query | `number` | no | Maximum number of labels to return. |
| `startIndex` | query | `number` | no | Zero-based label offset for pagination. |
