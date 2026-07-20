# WebinarGeek Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model WebinarGeek expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/list-broadcasts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## WebinarGeek actions that support pagination

- [List Broadcasts](actions/list-broadcasts.md)
- [List Messages](actions/list-messages.md)
- [List Questions](actions/list-questions.md)
- [List Subscription Payments](actions/list-subscription-payments.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Webinars](actions/list-webinars.md)
