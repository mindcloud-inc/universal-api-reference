# AMcards.com Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model AMcards.com expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## AMcards.com actions that support pagination

- [List Campaigns](actions/list-campaigns.md)
- [List Card Template Categories](actions/list-card-template-categories.md)
- [List Cards](actions/list-cards.md)
- [List Contacts](actions/list-contacts.md)
- [List Groups](actions/list-groups.md)
- [List Mailings](actions/list-mailings.md)
- [List Public Templates](actions/list-public-templates.md)
- [List Quicksend Templates](actions/list-quicksend-templates.md)
- [List Templates](actions/list-templates.md)
- [List Users](actions/list-users.md)
