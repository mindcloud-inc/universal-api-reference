# List Groups with Uploadcare

Retrieves all groups from your Uploadcare project.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [List Groups](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Group/operation/groupsList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Start listing groups created after this ISO 8601 timestamp. |
| `ordering` | query | `string` | no | Sort order for returned groups. |
