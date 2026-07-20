# Remove Project Member with Zeplin

Removes a member from a Zeplin project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/members/{member_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Remove Project Member](https://docs.zeplin.dev/reference/removeprojectmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `member_id` | path | `string` | yes | Member id |
