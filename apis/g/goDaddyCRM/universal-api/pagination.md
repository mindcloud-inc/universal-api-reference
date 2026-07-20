# GoDaddy CRM Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model GoDaddy CRM expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/get-dns-records?connectionId=$CONNECTION_ID&limit=25&offset=0&domain=example.com&type=A&name=%40" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## GoDaddy CRM actions that support pagination

- [Get DNS Records](actions/get-dns-records.md)
- [List Customer Certificates](actions/list-customer-certificates.md)
- [List Subscriptions](actions/list-subscriptions.md)
