# <img src="https://images.mindcloud.co/apps/icons/starshipit_1773945470759.png" alt="Starshipit logo" width="28" height="28"> Starshipit: Universal API

Manage shipping orders, labels, tracking, rates, and manifests

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/starshipit/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://starshipit.com
- **Vendor API docs:** https://api-docs.starshipit.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders (Unshipped)](actions/list-orders-unshipped.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-unshipped?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Add Address](actions/add-address.md) | POST |  |
| [Delete Address](actions/delete-address.md) | DELETE |  |
| [List Filtered Addresses](actions/list-filtered-addresses.md) | GET |  |
| [Update Address](actions/update-address.md) | PUT |  |

### Delivery Service

| Action | Method | Description |
| --- | --- | --- |
| [Delivery Services](actions/delivery-services.md) | GET |  |

### Manifest

| Action | Method | Description |
| --- | --- | --- |
| [List Manifests](actions/list-manifests.md) | GET |  |
| [Manifest by Carrier](actions/manifest-by-carrier.md) | PUT |  |
| [Manifest Orders (Orders)](actions/manifest-orders-orders.md) | PUT |  |
| [Manifest Orders (Shipments)](actions/manifest-orders-shipments.md) | PUT |  |

### Manifest File

| Action | Method | Description |
| --- | --- | --- |
| [List Manifest Files](actions/list-manifest-files.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Archive Order](actions/archive-order.md) | PUT |  |
| [Assign Orders](actions/assign-orders.md) | PUT |  |
| [Batch Update Orders](actions/batch-update-orders.md) | PUT |  |
| [Create Order](actions/create-order.md) | POST |  |
| [Create Orders](actions/create-orders.md) | POST |  |
| [Create Tracking Only Order](actions/create-tracking-only-order.md) | POST |  |
| [Delete Order](actions/delete-order.md) | DELETE |  |
| [Get Order(s)](actions/get-order-s.md) | GET |  |
| [List Orders (Delivered)](actions/list-orders-delivered.md) | GET |  |
| [List Orders (Printed or Unmanifested)](actions/list-orders-printed-or-unmanifested.md) | GET |  |
| [List Orders (Shipped)](actions/list-orders-shipped.md) | GET |  |
| [List Orders Summary](actions/list-orders-summary.md) | GET |  |
| [List Orders (Unshipped)](actions/list-orders-unshipped.md) | GET |  |
| [List Suggested Merges](actions/list-suggested-merges.md) | GET |  |
| [Merge Orders](actions/merge-orders.md) | PUT |  |
| [Print Packing Slips](actions/print-packing-slips.md) | PUT |  |
| [Restore Order](actions/restore-order.md) | PUT |  |
| [Search Orders](actions/search-orders.md) | GET |  |
| [Update Order](actions/update-order.md) | PUT |  |
| [Update Orders](actions/update-orders.md) | PUT |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Add Product](actions/add-product.md) | POST |  |
| [Delete Product or All Products](actions/delete-product-or-all-products.md) | DELETE |  |
| [Search Products](actions/search-products.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Rates](actions/get-rates.md) | GET |  |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Clone Shipment](actions/clone-shipment.md) | POST |  |
| [Print Label](actions/print-label.md) | POST |  |
| [Print Labels](actions/print-labels.md) | POST |  |
| [Replace Shipment](actions/replace-shipment.md) | PUT |  |

### Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Tracking Details](actions/get-tracking-details.md) | GET |  |

