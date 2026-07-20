# Zoho Assist Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zoho Assist expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-session-reports?connectionId=$CONNECTION_ID&limit=25&offset=0&type=all&fromDate=1&toDate=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zoho Assist actions that support pagination

- [List Session Reports](actions/list-session-reports.md)
- [List Unattended Computers](actions/list-unattended-computers.md)
