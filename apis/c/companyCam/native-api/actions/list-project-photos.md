# List Project Photos with CompanyCam

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:projectId/photos`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [List Project Photos](https://docs.companycam.com/reference/listprojectphotos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | — |
| `start_date` | query | `date` | no | Timestamp to return only photos captured on or after the provided value. |
| `end_date` | query | `date` | no | A timestamp to return photos captured on or before the provided value. |
| `user_ids` | query | `list<number>` | no | Filter results to include photos captured by one of these user IDs Send multiple values as a array. |
| `group_ids` | query | `list<number>` | no | Filter results to include photos captured by users in one of these group IDs Send multiple values as a array. |
| `tag_ids` | query | `list<number>` | no | Filter results to include photos with one of these tag IDs Send multiple values as a array. |
