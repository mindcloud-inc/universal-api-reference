# Get Export URL with Mural

Retrieves a mural export URL from Mural.

## Endpoint

- **Method:** `GET`
- **Path:** `/murals/:muralId/exports/:exportId`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Get Export URL](https://developers.mural.co/public/reference/exporturlmural)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `muralId` | path | `string` | yes |
| `exportId` | path | `string` | yes |
