# Update Form Tracking with Leadboxer

Updates form tracking settings for a dataset in Leadboxer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/datasets/{{datasetId}}/form-tracking`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Update Form Tracking](https://developers.leadboxer.com/reference/updateformtracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formTracking` | query | `boolean` | yes | Whether form tracking is enabled. |
| `allowIpMasking` | query | `boolean` | yes | Whether IP masking is allowed. |
| `formInputAttribute` | query | `string` | yes | The form input attribute to track. |
| `datasetId` | path | `string` | yes | The dataset ID. |
| `email` | query | `string` | yes | The user email address. |
