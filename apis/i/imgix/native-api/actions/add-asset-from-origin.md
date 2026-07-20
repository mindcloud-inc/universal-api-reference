# Add Asset From Origin with imgix

Adds an asset from origin to imgix.

## Endpoint

- **Method:** `POST`
- **Path:** `sources/:sourceId/assets/add/:originPath`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Add Asset From Origin](https://docs.imgix.com/en-US/apis/management/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `originPath` | path | `string` | yes | The origin path for the asset. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
