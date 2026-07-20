# List Team Members with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/team/members`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [List Team Members](https://docs.checkflow.io/docs/api/team#get-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nameContains` | query | `string` | no | Filters results to members whose name contains this string. Leave empty to return all members. |
