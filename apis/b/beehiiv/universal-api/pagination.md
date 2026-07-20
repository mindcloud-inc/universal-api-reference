# Beehiiv Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Beehiiv expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-bulk-subscription-updates?connectionId=$CONNECTION_ID&limit=25&offset=0&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Beehiiv actions that support pagination

- [List Bulk Subscription Updates](actions/list-bulk-subscription-updates.md)
- [List Publication Email Blasts](actions/list-publication-email-blasts.md)
- [List Publication Posts](actions/list-publication-posts.md)
- [List Publications](actions/list-publications.md)
- [List Subscriptions](actions/list-subscriptions.md)
