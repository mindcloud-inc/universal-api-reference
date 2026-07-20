# Delete Completed Job with DeepImage

Deletes a completed processing job from DeepImage.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest_api/result/:hash`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Delete Completed Job](https://documentation.deep-image.ai/api-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | path | `string` | yes | The completed processing job hash to delete from DeepImage. |
