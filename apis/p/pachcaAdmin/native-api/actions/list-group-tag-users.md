# List Group Tag Users with Pachca (Admin)

## Endpoint

- **Method:** `GET`
- **Path:** `/group_tags/:id/users`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [List Group Tag Users](https://dev.pachca.com/api/group-tags/get-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Pagination cursor from meta.paginate.next_page. |
| `id` | path | `number` | yes | Group tag id. |
| `limit` | query | `number` | no | Number of results to return. |
