# List Groups with Google Workspace Admin

Retrieves groups from Google Workspace Admin.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/groups`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [List Groups](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | query | `string` | yes | Google customer identifier. Use my_customer for current tenant. |
| `domain` | query | `string` | no | Optional domain to limit listed groups to one domain. |
| `orderBy` | query | `string` | no | Field to sort groups by, for example email. |
| `pageToken` | query | `string` | no | Pagination token from a previous groups list response. |
| `query` | query | `string` | no | Search query for matching groups. |
| `sortOrder` | query | `string` | no | Sort direction for the results. |
| `userKey` | query | `string` | no | Only list groups that include this user as a member. |
| `maxResults` | query | `number` | no | Maximum number of users to return per page. |
