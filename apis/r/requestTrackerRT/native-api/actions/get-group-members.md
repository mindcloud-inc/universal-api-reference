# Get Group Members with Request Tracker (RT)

Retrieves a group's members from Request Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `group/:groupId/members`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Get Group Members](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Group-Members)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The RT group ID. |
| `groups` | query | `boolean` | no | Set to false to exclude subgroup members from the result. |
| `recursively` | query | `boolean` | no | Set to true to include indirect nested group members recursively. |
| `users` | query | `boolean` | no | Set to false to exclude user members from the result. |
