# WaiverFile Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model WaiverFile expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waiver-data?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z&includeCustomColumns=true&consolidateParticipants=true&pageIndex=1&pageSize=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## WaiverFile actions that support pagination

- [List Waiver Data](actions/list-waiver-data.md)
- [List Waivers by Date Range](actions/list-waivers-by-date-range.md)
