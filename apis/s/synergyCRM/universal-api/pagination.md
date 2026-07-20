# SynergyCRM Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SynergyCRM expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synergyCRM/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SynergyCRM actions that support pagination

- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Deal Stage Categories](actions/list-deal-stage-categories.md)
- [List Deal Stages](actions/list-deal-stages.md)
- [List Deal Statuses](actions/list-deal-statuses.md)
- [List Deals](actions/list-deals.md)
- [List Diary Tasks](actions/list-diary-tasks.md)
- [List Entries](actions/list-entries.md)
- [List Order Statuses](actions/list-order-statuses.md)
- [List Orders](actions/list-orders.md)
- [List Product Categories](actions/list-product-categories.md)
- [List Product Statuses](actions/list-product-statuses.md)
- [List Product Types](actions/list-product-types.md)
- [List Products](actions/list-products.md)
- [List Projects](actions/list-projects.md)
