# Refresh Asset with imgix

Refreshes an asset in imgix from origin.

## Endpoint

- **Method:** `POST`
- **Path:** `sources/:sourceId/assets/refresh/:originPath`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Refresh Asset](https://docs.imgix.com/en-US/apis/management/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `originPath` | path | `string` | yes | The origin path for the asset. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
