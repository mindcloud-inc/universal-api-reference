# List Videos with CompanyCam

Returns videos visible to the authenticated user, sorted by
capture date (most recent first).

## Endpoint

- **Method:** `GET`
- **Path:** `videos`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [List Videos](https://docs.companycam.com/reference/listvideos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | no | Timestamp to return videos captured on or after the provided value. |
| `end_date` | query | `date` | no | timestamp to return videos captured on or before the provided value |
| `project_ids` | query | `string` | no | Filter results to include videos captured at one of these Project IDs Send multiple values as a array. |
| `user_ids` | query | `list<number>` | no | Filter results to include videos captured by one of these user IDs. Send multiple values as a array. |
| `group_ids` | query | `list<number>` | no | Filter results to include videos captured by one of these group IDs Send multiple values as a array. |
| `tag_ids` | query | `list<number>` | no | Filter results to include videos tagged with one of these tag IDs Send multiple values as a array. |
