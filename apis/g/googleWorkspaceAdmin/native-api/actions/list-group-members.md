# List Group Members with Google Workspace Admin

Retrieves members from a Google Workspace Admin group.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/groups/:groupKey/members`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [List Group Members](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | Group email address, alias, or unique ID. |
| `includeDerivedMembership` | query | `boolean` | no | Include indirect memberships in the result. |
| `maxResults` | query | `number` | no | Maximum number of members to return (up to 200). |
| `pageToken` | query | `string` | no | Pagination token from a previous members list response. |
| `roles` | query | `string` | no | Filter members by role: OWNER, MANAGER, or MEMBER. |
