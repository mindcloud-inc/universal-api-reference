# Underdog Protocol Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Underdog Protocol expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/get-collection?connectionId=$CONNECTION_ID&limit=25&offset=0&collectionAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Underdog Protocol actions that support pagination

- [Get Collection](actions/get-collection.md)
- [Get Project](actions/get-project.md)
- [List Collections](actions/list-collections.md)
- [List Orgs](actions/list-orgs.md)
- [List Project NFTs](actions/list-project-nfts.md)
- [List Projects](actions/list-projects.md)
- [List Webhooks](actions/list-webhooks.md)
- [Search Project NFTs](actions/search-project-nfts.md)
