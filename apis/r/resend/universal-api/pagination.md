# Resend Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Resend expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-api-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Resend actions that support pagination

- [List API Keys](actions/list-api-keys.md)
- [List Audiences](actions/list-audiences.md)
- [List Broadcasts](actions/list-broadcasts.md)
- [List Domains](actions/list-domains.md)
- [List Received Emails](actions/list-received-emails.md)
- [List Sent Emails](actions/list-sent-emails.md)
- [List Templates](actions/list-templates.md)
- [List Webhooks](actions/list-webhooks.md)
