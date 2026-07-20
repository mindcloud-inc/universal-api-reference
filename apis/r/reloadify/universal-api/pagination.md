# Reloadify Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Reloadify expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-brand-products?connectionId=$CONNECTION_ID&limit=25&offset=0&languageId=string&brandId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Reloadify actions that support pagination

- [List Brand Products](actions/list-brand-products.md)
- [List Brands](actions/list-brands.md)
- [List Cart Products](actions/list-cart-products.md)
- [List Categories](actions/list-categories.md)
- [List Category Products](actions/list-category-products.md)
- [List Custom Attributes](actions/list-custom-attributes.md)
- [List Global Unsubscribes](actions/list-global-unsubscribes.md)
- [List Languages](actions/list-languages.md)
- [List Order Products](actions/list-order-products.md)
- [List Orders](actions/list-orders.md)
- [List Product Categories](actions/list-product-categories.md)
- [List Product Variants](actions/list-product-variants.md)
- [List Products](actions/list-products.md)
- [List Profiles](actions/list-profiles.md)
- [List Relevant Products](actions/list-relevant-products.md)
- [List Reviews](actions/list-reviews.md)
- [List Shopping Carts](actions/list-shopping-carts.md)
- [List Variants](actions/list-variants.md)
