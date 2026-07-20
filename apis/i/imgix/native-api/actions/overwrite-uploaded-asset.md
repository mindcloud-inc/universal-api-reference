# Overwrite Uploaded Asset with imgix

Overwrites an uploaded asset in an imgix source.

## Endpoint

- **Method:** `POST`
- **Path:** `sources/:sourceId/upload/:originPath`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Overwrite Uploaded Asset](https://docs.imgix.com/en-US/apis/management/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `originPath` | path | `string` | yes | The destination origin path for the uploaded asset. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
