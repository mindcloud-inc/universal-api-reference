# Cryptlex Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Cryptlex expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/list-activations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Cryptlex actions that support pagination

- [List Activations](actions/list-activations.md)
- [List Licenses](actions/list-licenses.md)
- [List Products](actions/list-products.md)
- [List Releases](actions/list-releases.md)
- [List Users](actions/list-users.md)
- [List Webhooks](actions/list-webhooks.md)
