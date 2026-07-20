# Alto Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Alto expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/filter-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Alto actions that support pagination

- [Filter Inventory](actions/filter-inventory.md)
- [Filter Listings](actions/filter-listings.md)
- [Get All Contacts](actions/get-all-contacts.md)
- [Get Branches](actions/get-branches.md)
- [Get Documents](actions/get-documents.md)
- [Get Inventory](actions/get-inventory.md)
- [Get Inventory Documents](actions/get-inventory-documents.md)
- [Get Inventory Tenancies](actions/get-inventory-tenancies.md)
- [Get Landlords](actions/get-landlords.md)
- [Get Leads](actions/get-leads.md)
- [Get Negotiator Appointments](actions/get-negotiator-appointments.md)
- [Get Negotiators](actions/get-negotiators.md)
- [Get Owners](actions/get-owners.md)
- [Get Suppliers](actions/get-suppliers.md)
- [Get Tenancies](actions/get-tenancies.md)
- [Get Valuations](actions/get-valuations.md)
- [Search Contacts](actions/search-contacts.md)
- [Search Inventory](actions/search-inventory.md)
