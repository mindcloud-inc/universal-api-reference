# Geral Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Geral expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-account-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Geral actions that support pagination

- [List Account Logs](actions/list-account-logs.md)
- [List Collected Data](actions/list-collected-data.md)
- [List Domains](actions/list-domains.md)
- [List Links](actions/list-links.md)
- [List Notification Handlers](actions/list-notification-handlers.md)
- [List Payments](actions/list-payments.md)
- [List Pixels](actions/list-pixels.md)
- [List QR Codes](actions/list-qr-codes.md)
- [List Splash Pages](actions/list-splash-pages.md)
- [List Statistics](actions/list-statistics.md)
