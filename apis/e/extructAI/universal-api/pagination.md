# Extruct AI Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Extruct AI expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/find-similar-companies?connectionId=$CONNECTION_ID&limit=25&offset=0&company_identifier=trustpayments.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Extruct AI actions that support pagination

- [Find Similar Companies](actions/find-similar-companies.md)
- [Get Discovery Task Results](actions/get-discovery-task-results.md)
- [Get Table Data](actions/get-table-data.md)
- [List Discovery Tasks](actions/list-discovery-tasks.md)
- [List Tables](actions/list-tables.md)
- [Search Companies](actions/search-companies.md)
