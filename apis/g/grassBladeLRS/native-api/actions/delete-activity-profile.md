# Delete Activity Profile with GrassBlade LRS

Deletes an activity profile from GrassBlade LRS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/activities/profile`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Delete Activity Profile](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#actprofres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | query | `string` | yes |
| `profileId` | query | `string` | yes |
