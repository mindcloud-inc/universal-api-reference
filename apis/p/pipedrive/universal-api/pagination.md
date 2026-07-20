# Pipedrive Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Pipedrive expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Pipedrive actions that support pagination

- [Get Activities](actions/get-activities.md)
- [Get All Product Fields](actions/get-all-deal-fields-copy.md)
- [Get Organizations](actions/get-organizations.md)
- [Get Persons](actions/get-persons.md)
- [Get Products](actions/get-products.md)
- [List Deals](actions/list-deals.md)
- [Search Deals](actions/search-deals.md)
- [Search Leads](actions/search-leads.md)
- [Search Organizations](actions/search-organization.md)
- [Search Persons](actions/search-persons.md)
- [Search Products](actions/search-products.md)
