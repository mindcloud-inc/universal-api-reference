# List Project Videos with CompanyCam

Retrieve videos captured at a specified project.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:projectId/videos`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [List Project Videos](https://docs.companycam.com/reference/listprojectvideos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | ID of the Project |
| `startDate` | query | `date` | no | Timestamp to return videos captured on or after the provided value. |
| `endDate` | query | `date` | no | timestamp to return videos captured on or before the provided value |
| `userIds` | query | `list<number>` | no | Filter results to include videos captured by one of these user IDs. Send multiple values as a array. |
| `groupIds` | query | `list<number>` | no | Filter results to include videos captured by one of these group IDs Send multiple values as a array. |
| `tagIds` | query | `list<number>` | no | Filter results to include videos tagged with one of these tag IDs Send multiple values as a array. |
