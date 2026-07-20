# Teamgate Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Teamgate expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Teamgate actions that support pagination

- [List Activities](actions/list-activities.md)
- [List Companies](actions/list-companies.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Deals](actions/list-deals.md)
- [List Lead Activities](actions/list-lead-activities.md)
- [List Lead Statuses](actions/list-lead-statuses.md)
- [List Leads](actions/list-leads.md)
- [List People](actions/list-people.md)
- [List Person Deals](actions/list-person-deals.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Sources](actions/list-sources.md)
- [List Users](actions/list-users.md)
- [Search Companies](actions/search-companies.md)
- [Search Deals](actions/search-deals.md)
- [Search Leads](actions/search-leads.md)
- [Search People](actions/search-people.md)
