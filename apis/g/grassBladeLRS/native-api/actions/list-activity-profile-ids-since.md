# List Activity Profile IDs Since with GrassBlade LRS

Retrieves activity profile IDs from GrassBlade LRS since a timestamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/profile`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [List Activity Profile IDs Since](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#actprofres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | query | `string` | yes |
| `since` | query | `string` | yes |
