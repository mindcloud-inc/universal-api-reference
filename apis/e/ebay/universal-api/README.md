# <img src="https://images.mindcloud.co/apps/icons/e-bay_1782742794164.png" alt="eBay logo" width="28" height="28"> eBay: Universal API

Manage inventory, offers and listings in your Ebay store.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ebay/latest
- **Category:** Commerce
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ebay.com/
- **Vendor API docs:** https://developer.ebay.com/api-docs/static/gs_ebay-rest-getting-started-landing.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Inventory Items](actions/list-inventory-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-inventory-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [Get Category Sub-Tree](actions/get-category-sub-tree.md) | GET | Retrieves a category Sub-Tree. |
| [Get Category Suggestions](actions/get-category-suggestions.md) | GET | Retrieve a categories that are considered by eBay to most closely correspond to the provided query. |
| [Get Category Tree](actions/get-category-tree.md) | GET | Retrieves a complete category tree by its ID. |
| [Get Default Category Tree](actions/get-default-category-tree.md) | GET |  |
| [List Item Aspects for Category](actions/list-item-aspects-for-category.md) | GET | Returns a complete list of aspects for all of the leaf categories that belong to an eBay marketplace. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Migrate Listings](actions/bulk-migrate-listings.md) | POST | Create a new Inventory Location. |
| [Create Inventory Location](actions/create-inventory-location.md) | POST | Create a new Inventory Location. |
| [Create or Replace Inventory Item](actions/create-or-replace-inventory-item.md) | POST |  |
| [Get Inventory Item](actions/get-inventory-item.md) | GET |  |
| [Get SKU Inventory Location](actions/get-sku-inventory-location.md) | GET | Allows sellers to retrieve the locations mapped to a specific SKU within a listing. |
| [List Inventory Items](actions/list-inventory-items.md) | GET |  |
| [List Inventory Locations](actions/list-inventory-locations.md) | GET | Retrieves all defined details for every inventory location associated with the authenticated seller's account. |
| [List Seller Items](actions/list-seller-items.md) | GET | Retrieve items listed by the authenticated user, including item data. |
| [List Seller Items_v2](actions/list-seller-items-v2.md) | GET | Retrieve items listed by the authenticated user, including item data. |

### Offers / Listings

| Action | Method | Description |
| --- | --- | --- |
| [Create Offer](actions/create-offer.md) | POST | Creates an offer for a specific inventory item on a specific eBay marketplace. It is up to the sellers whether they want to create a… |
| [Delete Offer](actions/delete-offer.md) | DELETE |  |
| [Get Item Condition Policies](actions/get-item-condition-policies.md) | GET |  |
| [Get Offer](actions/get-offer.md) | GET | Retrieve an Offer by it's unique offer ID. |
| [List Offers by SKU](actions/get-offers.md) | GET | Retrieves all existing offers for the specified SKU value. With options to limit the retrieved offers to a specific eBay marketplace, or a… |
| [Publish Offer](actions/publish-offer.md) | PUT | Convert an unpublished offer into a published offer (or live eBay listing). |
| [Update Offer](actions/update-offer.md) | POST | Updates an offer for a specific inventory item on a specific eBay marketplace. It is up to the sellers whether they want to create a… |
| [Withdraw Offer](actions/withdraw-offer.md) | PUT | End a single-variation listing |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Orders](actions/get-orders.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET |  |
| [Update - Price and Quantity](actions/update-price-and-quantity.md) | PUT |  |

### Payouts

| Action | Method | Description |
| --- | --- | --- |
| [Get Payout](actions/get-payout.md) | GET |  |
| [List Payouts](actions/list-payouts.md) | GET |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Use this call to retrieve the contents of an order based on its unique identifier, orderId. This value is returned in the getOrders call's… |
| [List Orders](actions/list-orders.md) | GET |  |

### Seller Programs

| Action | Method | Description |
| --- | --- | --- |
| [List Opted-In Programs](actions/list-opted-in-programs.md) | GET | Retrieve a list of the seller programs that the authenticated seller has opted-in to. |
| [Opt-In to Program](actions/opt-in-to-program.md) | PUT | This method opts the seller in to an eBay seller program. Refer to the Account API overview for information about available eBay seller… |
| [Opt-Out of Program](actions/opt-out-of-program.md) | PUT | This method opts the seller out of an eBay seller program. Refer to the Account API overview for information about available eBay seller… |

### Selling Policy Management

| Action | Method | Description |
| --- | --- | --- |
| [Create a Selling Policy](actions/create-seller-policy.md) | GET | Retrieve a specific list of seller policies (i.e. fulfillment, payment & return policies) |
| [List Selling Policies](actions/list-selling-policies.md) | GET | Retrieve a specific list of selling policies (i.e. fulfillment, payment & return policies) |

### Trading Api

| Action | Method | Description |
| --- | --- | --- |
| [Complete Sale](actions/complete-sale.md) | PUT | Use this call to do various tasks after the creation of a single line item or multiple line item order. |
| [Get Seller Events](actions/get-seller-events.md) | GET | Use this call to retrieve a list of the items on which a seller event has occurred. A seller event includes actions such as a revision to… |
| [Revise Inventory Status](actions/revise-inventory-status.md) | PUT | Change the price and/or quantity of up to four active, fixed-price listings. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Payout Transactions](actions/list-payout-transactions.md) | GET |  |

