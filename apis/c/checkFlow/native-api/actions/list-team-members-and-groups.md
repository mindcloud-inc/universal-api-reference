# List Team Members And Groups with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/team/members-and-groups`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [List Team Members And Groups](https://docs.checkflow.io/docs/api/team#get-members-and-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nameContains` | query | `string` | no | Filters results to members and groups whose name contains this string. Leave empty to return all. |
