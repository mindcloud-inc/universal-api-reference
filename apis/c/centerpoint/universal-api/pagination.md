# Centerpoint Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Centerpoint expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-budget-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Centerpoint actions that support pagination

- [List Budget Entries](actions/list-budget-entries.md)
- [List Budget Types](actions/list-budget-types.md)
- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Cost Codes](actions/list-cost-codes.md)
- [List Employees](actions/list-employees.md)
- [List Invoices](actions/list-invoices.md)
- [List Materials](actions/list-materials.md)
- [List Model Files](actions/list-model-files.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Product Templates](actions/list-product-templates.md)
- [List Production Days](actions/list-production-days.md)
- [List Production Items](actions/list-production-items.md)
- [List Production Materials](actions/list-production-materials.md)
- [List Production Materials by Production](actions/list-production-materials-by-production.md)
- [List Production Purchase Orders](actions/list-production-purchase-orders.md)
- [List Productions](actions/list-productions.md)
- [List Productions With Domain Production Only](actions/list-productions-with-domain-production-only.md)
- [List Products](actions/list-products.md)
- [List Properties](actions/list-properties.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Service Agreements](actions/list-service-agreements.md)
- [List Services](actions/list-services.md)
- [List Tasks](actions/list-tasks.md)
- [List Tax Codes](actions/list-tax-codes.md)
- [List Warranties](actions/list-warranties.md)
- [List Work Time Entries](actions/list-work-time-entries.md)
