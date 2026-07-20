# Bluebarry Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Bluebarry expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-advisors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Bluebarry actions that support pagination

- [List Advisors](actions/list-advisors.md)
- [List Answers](actions/list-answers.md)
- [List Landing Pages](actions/list-landing-pages.md)
- [List Live Product Feeds](actions/list-live-product-feeds.md)
- [List Products](actions/list-products.md)
- [List Questions](actions/list-questions.md)
- [List Settings](actions/list-settings.md)
- [List Webhook Subscriptions](actions/list-webhook-subscriptions.md)
