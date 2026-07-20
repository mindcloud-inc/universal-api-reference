# ProfitWell Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ProfitWell expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/list-retain-unsubscribed-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&interventionType=reactivation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ProfitWell actions that support pagination

- [List Retain Unsubscribed Customers](actions/list-retain-unsubscribed-customers.md)
- [Search Customers](actions/search-customers.md)
