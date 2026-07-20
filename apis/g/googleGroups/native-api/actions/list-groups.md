# List Groups with Google Groups

Retrieves groups from Google Groups for a domain or user.

## Endpoint

- **Method:** `GET`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [List Groups](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search expression for Google Groups. |
| `maxResults` | query | `number` | no | Maximum number of groups to return per page. |
| `orderBy` | query | `string` | no | Field to sort by. Accepted values: `0`. |
| `sortOrder` | query | `string` | no | Sort direction when orderBy is provided. Accepted values: `0`, `1`. |
| `domain` | query | `string` | no | Limit results to a single domain instead of the full customer. |
| `userKey` | query | `string` | no | List only groups that the specified user belongs to. |
| `pageToken` | query | `string` | no | Token for the next page of results. |
