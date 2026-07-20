# <img src="https://images.mindcloud.co/apps/icons/corporate-merch-icon_1775161700067.png" alt="Corporate Merch logo" width="28" height="28"> Corporate Merch: Universal API

Corporate Merch is a swag-management platform for designs, catalogs, orders, shipments, wallets, and organization operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/corporateMerch/latest
- **Category:** Commerce
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.corporatemerch.com
- **Vendor API docs:** https://corporatemerch.readme.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Catalog](actions/list-catalog.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/list-catalog?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Assign Designs To Organization](actions/assign-designs-to-organization.md) | PUT | Assigns designs to an organization in Corporate Merch. |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in Corporate Merch. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves all organizations from Corporate Merch. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Corporate Merch. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Design](actions/create-design.md) | POST | Creates a new design in Corporate Merch. |
| [Customize Product](actions/customize-product.md) | POST | Creates a customized product design in Corporate Merch. |
| [Customize Product Async](actions/customize-product-async.md) | POST | Creates a customized product design asynchronously in Corporate Merch. |
| [Delete Design](actions/delete-design.md) | DELETE | Deletes an existing design from Corporate Merch. |
| [Get Catalog By Id](actions/get-catalog-by-id.md) | GET | Retrieves a catalog product from Corporate Merch. |
| [Get Catalog Estimated Ship Date](actions/get-catalog-estimated-ship-date.md) | GET | Retrieves a catalog product's estimated ship date from Corporate Merch. |
| [Get Design By Id](actions/get-design-by-id.md) | GET | Retrieves a design from Corporate Merch. |
| [Get Design Estimated Ship Date](actions/get-design-estimated-ship-date.md) | GET | Retrieves a design's estimated ship date from Corporate Merch. |
| [List Catalog](actions/list-catalog.md) | GET | Retrieves catalog products from Corporate Merch. |
| [List Designs](actions/list-designs.md) | GET | Retrieves all designs from Corporate Merch. |
| [List Organization Designs](actions/list-organization-designs.md) | GET | Retrieves designs for an organization in Corporate Merch. |
| [Update Customized Product](actions/update-customized-product.md) | PUT | Updates a customized product design in Corporate Merch. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | DELETE | Cancels an existing order in Corporate Merch. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Corporate Merch. |
| [Get Order By Id](actions/get-order-by-id.md) | GET | Retrieves an order from Corporate Merch. |
| [List Orders](actions/list-orders.md) | GET | Retrieves all orders from Corporate Merch. |
| [Update Order Address](actions/update-order-address.md) | PUT | Updates an order address in Corporate Merch. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipment By Id](actions/get-shipment-by-id.md) | GET | Retrieves a shipment from Corporate Merch. |
| [List Order Shipments](actions/list-order-shipments.md) | GET | Retrieves shipments for an order in Corporate Merch. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves the credit balance from Corporate Merch. |
| [Get Order Quote](actions/get-order-quote.md) | GET | Retrieves an order quote from Corporate Merch. |

