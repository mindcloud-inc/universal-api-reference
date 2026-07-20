# InflatableOffice Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model InflatableOffice expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## InflatableOffice actions that support pagination

- [List Categories](actions/list-categories.md)
- [List Categories By Location](actions/list-categories-by-location.md)
- [List Categories By WordPress Sync](actions/list-categories-by-word-press-sync.md)
- [List Customers](actions/list-customers.md)
- [List Detailed Customers](actions/list-detailed-customers.md)
- [List Detailed Leads](actions/list-detailed-leads.md)
- [List Leads](actions/list-leads.md)
- [List Leads By Saved Filter](actions/list-leads-by-saved-filter.md)
- [List Rentals](actions/list-rentals.md)
- [List Rentals By Category](actions/list-rentals-by-category.md)
- [List Rentals For Quote Page / Brand](actions/list-rentals-for-quote-page-brand.md)
- [List Rentals With Price Details](actions/list-rentals-with-price-details.md)
- [List Vehicles](actions/list-vehicles.md)
- [List Workers](actions/list-workers.md)
