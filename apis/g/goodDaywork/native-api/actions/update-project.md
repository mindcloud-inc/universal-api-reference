# Update Project with GoodDay.work

Updates an existing project in GoodDay.work.

## Endpoint

- **Method:** `PUT`
- **Path:** `/project/:projectId`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [Update Project](https://www.goodday.work/developers/api-v2/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | GoodDay project ID. |
| `userId` | body | `string` | yes | User on behalf of whom API executes update. |
| `progress` | body | `number` | no | Project progress percentage 0-100. |
