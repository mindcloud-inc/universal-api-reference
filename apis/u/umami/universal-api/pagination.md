# Umami Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Umami expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-expanded-website-metrics?connectionId=$CONNECTION_ID&limit=25&offset=0&websiteId=string&startAt=1&endAt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Umami actions that support pagination

- [Get Expanded Website Metrics](actions/get-expanded-website-metrics.md)
- [Get Website Metrics](actions/get-website-metrics.md)
- [List Event Data](actions/list-event-data.md)
- [List Events](actions/list-events.md)
- [List Sessions](actions/list-sessions.md)
- [List Websites](actions/list-websites.md)
