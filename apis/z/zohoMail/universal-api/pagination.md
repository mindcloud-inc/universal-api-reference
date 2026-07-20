# Zoho Mail Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zoho Mail expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-emails?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=3048445000000008002" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zoho Mail actions that support pagination

- [List Emails](actions/list-emails.md)
- [Search Emails](actions/search-emails.md)
