# Update Asset with imgix

Updates an asset in imgix.

## Endpoint

- **Method:** `PATCH`
- **Path:** `sources/:sourceId/assets/:originPath`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Update Asset](https://docs.imgix.com/en-US/apis/management/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `originPath` | path | `string` | yes | The origin path for the asset in the source. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
