# Create Activity Profile with GrassBlade LRS

Stores or updates an activity profile in GrassBlade LRS.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities/profile`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Create Activity Profile](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#actprofres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | query | `string` | yes |
| `profileId` | query | `string` | yes |
| `document` | body | `object` | yes |
