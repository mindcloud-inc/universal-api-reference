# Get Group with Google Workspace Admin

Retrieves a group from Google Workspace Admin.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/groups/:groupKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Get Group](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | Group email address, alias, or unique ID. |
