# List State IDs with GrassBlade LRS

Retrieves state document IDs from GrassBlade LRS.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/state`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [List State IDs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | query | `string` | yes |
| `agent` | query | `string` | yes |
