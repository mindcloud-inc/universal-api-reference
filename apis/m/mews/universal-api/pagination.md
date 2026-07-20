# Mews Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Mews expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-accounting-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Mews actions that support pagination

- [Get All Accounting Categories](actions/get-all-accounting-categories.md)
- [Get All Age Categories](actions/get-all-age-categories.md)
- [Get All Business Segments](actions/get-all-business-segments.md)
- [Get All Cashiers](actions/get-all-cashiers.md)
- [Get All Companies](actions/get-all-companies.md)
- [Get All Counters](actions/get-all-counters.md)
- [Get All Departments](actions/get-all-departments.md)
- [Get All Outlets](actions/get-all-outlets.md)
- [Get All Resource Categories](actions/get-all-resource-categories.md)
- [Get All Resource Features](actions/get-all-resource-features.md)
- [Get All Resources](actions/get-all-resources.md)
- [Get All Services](actions/get-all-services.md)
- [Get All Sources](actions/get-all-sources.md)
- [Get All Tasks](actions/get-all-tasks.md)
