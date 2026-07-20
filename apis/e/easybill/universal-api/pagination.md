# easybill Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model easybill expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easybill/latest/actions/get-position-discount?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## easybill actions that support pagination

- [Get Position Discount](actions/get-position-discount.md)
- [Get Position Group Discount](actions/get-position-group-discount.md)
- [List Attachments](actions/list-attachments.md)
- [List Customers](actions/list-customers.md)
- [List Documents](actions/list-documents.md)
- [List Logins](actions/list-logins.md)
- [List Position Discounts](actions/list-position-discounts.md)
- [List Position Group Discounts](actions/list-position-group-discounts.md)
- [List Position Groups](actions/list-position-groups.md)
- [List Positions](actions/list-positions.md)
- [List Post Boxes](actions/list-post-boxes.md)
- [List Projects](actions/list-projects.md)
- [List Serial Numbers](actions/list-serial-numbers.md)
- [List Stocks](actions/list-stocks.md)
- [List Tasks](actions/list-tasks.md)
- [List Text Templates](actions/list-text-templates.md)
- [List Time Trackings](actions/list-time-trackings.md)
- [List WebHooks](actions/list-web-hooks.md)
