# Wisewand Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Wisewand expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-all-authors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Wisewand actions that support pagination

- [Get all authors](actions/get-all-authors.md)
- [Get all categories](actions/get-all-categories.md)
- [List articles](actions/list-articles.md)
- [List categorypages](actions/list-categorypages.md)
- [List connections](actions/list-connections.md)
- [List discoverarticles](actions/list-discoverarticles.md)
- [List feeds](actions/list-feeds.md)
- [List personas](actions/list-personas.md)
- [List productpages](actions/list-productpages.md)
- [List projects](actions/list-projects.md)
- [List transactions](actions/list-transactions.md)
- [List updateposts](actions/list-updateposts.md)
