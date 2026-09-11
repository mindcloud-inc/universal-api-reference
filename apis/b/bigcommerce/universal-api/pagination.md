# BigCommerce Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model BigCommerce expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-all-countries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## BigCommerce actions that support pagination

- [Create Customer Address](actions/create-customer-address.md)
- [Create Products Channel Assignments](actions/create-products-channel-assignments.md)
- [Get All Countries](actions/get-all-countries.md)
- [Get All Customers](actions/get-all-customers.md)
- [Get All Customers (v2)](actions/get-all-customers-v2.md)
- [Get All States By Country](actions/get-all-states-by-country.md)
- [Get Channel Listings](actions/get-channel-listings.md)
- [Get Companies](actions/get-companies.md)
- [Get Orders](actions/get-orders.md)
- [Get Product Channel Assignments](actions/get-product-channel-assignments.md)
- [Get Products](actions/get-products.md)
- [List Customer Addresses](actions/list-customer-addresses.md)
- [Update Customer Address](actions/update-customer-address.md)
