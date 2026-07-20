# Get Processing Job Result with DeepImage

Retrieves a completed processing job result from DeepImage.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest_api/result/:hash`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Get Processing Job Result](https://documentation.deep-image.ai/account-and-settings/account-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | path | `string` | yes | The processing job hash returned by Queue Image Processing Job or a wrapper action. |
