# List Team Groups with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/team/groups`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [List Team Groups](https://docs.checkflow.io/docs/api/team#get-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nameContains` | query | `string` | no | Filters results to groups whose name contains this string. Leave empty to return all. |
