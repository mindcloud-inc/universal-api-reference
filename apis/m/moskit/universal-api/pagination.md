# Moskit Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Moskit expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Moskit actions that support pagination

- [List Activities](actions/list-activities.md)
- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Projects](actions/list-projects.md)
- [List Users](actions/list-users.md)
- [Search Activities](actions/search-activities.md)
- [Search Companies](actions/search-companies.md)
- [Search Contacts](actions/search-contacts.md)
- [Search Deals](actions/search-deals.md)
- [Search Projects](actions/search-projects.md)
