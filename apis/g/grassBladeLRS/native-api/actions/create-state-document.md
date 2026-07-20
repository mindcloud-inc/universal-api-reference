# Create State Document with GrassBlade LRS

Stores or updates a state document in GrassBlade LRS.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities/state`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Create State Document](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | query | `string` | yes |
| `agent` | query | `string` | yes |
| `stateId` | query | `string` | yes |
| `registration` | query | `string` | no |
| `document` | body | `object` | yes |
