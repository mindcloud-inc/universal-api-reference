# Dealfront Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Dealfront expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-custom-feed-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&customFeedId=string&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Dealfront actions that support pagination

- [List Custom Feed Leads](actions/list-custom-feed-leads.md)
- [List Lead Visits](actions/list-lead-visits.md)
- [List Leads](actions/list-leads.md)
- [List Visits](actions/list-visits.md)
