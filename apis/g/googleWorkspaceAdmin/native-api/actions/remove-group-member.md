# Remove Group Member with Google Workspace Admin

Removes a member from a Google Workspace Admin group.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/admin/directory/v1/groups/:groupKey/members/:memberKey`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Remove Group Member](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | Group email address, alias, or unique ID. |
| `memberKey` | path | `string` | yes | Member email address, alias, or unique ID. |
