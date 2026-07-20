# Get Group Member with Google Workspace Admin

Retrieves a member from a Google Workspace Admin group.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/groups/:groupKey/members/:memberKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Get Group Member](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | Group email address, alias, or unique ID. |
| `memberKey` | path | `string` | yes | Member email address, alias, or unique ID. |
