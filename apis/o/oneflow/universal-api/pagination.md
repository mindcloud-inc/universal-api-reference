# Oneflow Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Oneflow expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Oneflow actions that support pagination

- [List Contacts](actions/list-contacts.md)
- [List Contract Data Fields](actions/list-contract-data-fields.md)
- [List Contract Files](actions/list-contract-files.md)
- [List Contracts](actions/list-contracts.md)
- [List Parties](actions/list-parties.md)
- [List Template Types](actions/list-template-types.md)
- [List Templates](actions/list-templates.md)
- [List Users](actions/list-users.md)
- [List Workspaces](actions/list-workspaces.md)
