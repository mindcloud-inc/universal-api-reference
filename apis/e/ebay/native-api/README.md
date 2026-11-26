# eBay: Native API Reference

A consolidated summary of eBay's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://developer.ebay.com/api-docs/static/gs_ebay-rest-getting-started-landing.html
- **REST base URL:** `https://api.ebay.com/`
- **REST eBay XML base URL:** `https://api.ebay.com/ws/api.dll`
- **Sell Finances base URL:** `https://apiz.ebay.com/sell/finances/v1`

## Authentication

### OAuth 2.0

### Credentials

- **eBay Environment:** `eBayEnvironment` · optional
- **Client Secret Type:** `clientSecretType` · optional · This should be set to "Production" or "Sandbox" based on the eBay environment you are using.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.ebay.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.ebay.com/identity/v1/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://api.ebay.com/oauth/api_scope/sell.account https://api.ebay.com/oauth/api_scope/sell.account.readonly https://api.ebay.com/oauth/api_scope https://api.ebay.com/oauth/api_scope/sell.account.readonly https://api.ebay.com/oauth/api_scope/sell.inventory.readonly https://api.ebay.com/oauth/api_scope/sell.inventory https://api.ebay.com/oauth/api_scope/sell.fulfillment https://api.ebay.com/oauth/api_scope/sell.fulfillment.readonly https://api.ebay.com/oauth/api_scope/sell.stores.readonly`.

Refresh expired access tokens with a POST request to https://api.ebay.com/identity/v1/oauth2/token.

[Official authentication documentation](https://developer.ebay.com/api-docs/static/oauth-scopes.html)

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### REST eBay XML

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml` |

Responses from this API use XML.

### Sell Finances

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

- **REST:** Use `limit` in the query string to set the page size (default 25; accepted range 1–200). Use `offset` in the query string as the record offset.
- **REST eBay XML:** Use `limit` in the query string to set the page size (default 25; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.
- **Sell Finances:** Use `limit` in the query string to set the page size (default 20; accepted range 1–200). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

- **REST:** Wait 8000 ms before the first retry. Stop after 5 attempts. Multiply the delay by 3 after each failed attempt.

## Endpoints (38 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Bulk Migrate Listings](actions/bulk-migrate-listings.md) | REST | `POST sell/inventory/v1/bulk_migrate_listing` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/location/methods/createInventoryLocation) |
| [Complete Sale](actions/complete-sale.md) | REST eBay XML | `POST` | [docs](https://developer.ebay.com/devzone/xml/docs/reference/ebay/CompleteSale.html) |
| [Create Inventory Location](actions/create-inventory-location.md) | REST | `POST sell/inventory/v1/location/:merchantLocationKey` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/location/methods/createInventoryLocation) |
| [Create Offer](actions/create-offer.md) | REST | `POST sell/inventory/v1/offer` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/createOffer) |
| [Create or Replace Inventory Item](actions/create-or-replace-inventory-item.md) | REST | `PUT sell/inventory/v1/inventory_item/:sku` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/inventory_item/methods/createOrReplaceInventoryItem) |
| [Create a Selling Policy](actions/create-seller-policy.md) | REST | `POST sell/account/v1/:policy` | [docs](https://developer.ebay.com/api-docs/sell/account/resources/custom_policy/methods/getCustomPolicies) |
| [Delete Offer](actions/delete-offer.md) | REST | `DELETE sell/inventory/v1/offer/:offerId` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/deleteOffer) |
| [Get Category Sub-Tree](actions/get-category-sub-tree.md) | REST | `GET commerce/taxonomy/v1/category_tree/:categoryTreeID/get_category_subtree` | [docs](https://developer.ebay.com/api-docs/commerce/taxonomy/resources/category_tree/methods/getCategorySubtree) |
| [Get Category Suggestions](actions/get-category-suggestions.md) | REST | `GET commerce/taxonomy/v1/category_tree/0/get_category_suggestions` | [docs](https://developer.ebay.com/api-docs/commerce/taxonomy/resources/category_tree/methods/getCategorySuggestions) |
| [Get Category Tree](actions/get-category-tree.md) | REST | `GET commerce/taxonomy/v1/category_tree/:categoryTreeID` | [docs](https://developer.ebay.com/api-docs/commerce/taxonomy/resources/category_tree/methods/getCategoryTree) |
| [Get Default Category Tree](actions/get-default-category-tree.md) | REST | `GET commerce/taxonomy/v1/get_default_category_tree_id` | [docs](https://developer.ebay.com/api-docs/commerce/taxonomy/resources/category_tree/methods/getDefaultCategoryTreeId) |
| [Get Inventory Item](actions/get-inventory-item.md) | REST | `GET sell/inventory/v1/inventory_item/:sku` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/inventory_item/methods/getInventoryItem) |
| [Get Item](actions/get-item.md) | REST eBay XML | `GET` |  |
| [Get Item Condition Policies](actions/get-item-condition-policies.md) | REST | `GET sell/metadata/v1/marketplace/EBAY_US/get_item_condition_policies` | [docs](https://developer.ebay.com/api-docs/sell/metadata/resources/marketplace/methods/getItemConditionPolicies) |
| [Get Offer](actions/get-offer.md) | REST | `GET sell/inventory/v1/offer/:offerID` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/getOffer) |
| [List Offers by SKU](actions/get-offers.md) | REST | `GET sell/inventory/v1/offer` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/getOffers) |
| [Get Order](actions/get-order.md) | REST | `GET sell/fulfillment/v1/order/{orderID}` | [docs](https://developer.ebay.com/api-docs/sell/fulfillment/resources/order/methods/getOrders) |
| [Get Orders](actions/get-orders.md) | REST eBay XML | `POST` | [docs](https://developer.ebay.com/devzone/xml/docs/reference/ebay/getorders.html) |
| [Get Payout](actions/get-payout.md) | Sell Finances | `GET /payout/:payoutId` | [docs](https://developer.ebay.com/develop/api/sell/finances_api/payout/getPayout) |
| [Get Seller Events](actions/get-seller-events.md) | REST eBay XML | `POST` | [docs](https://developer.ebay.com/devzone/xml/docs/reference/ebay/GetSellerEvents.html) |
| [Get SKU Inventory Location](actions/get-sku-inventory-location.md) | REST | `GET sell/inventory/v1/listing/:listingID/sku/:sku/locations` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/listing/methods/getSkuLocationMapping) |
| [List Inventory Items](actions/list-inventory-items.md) | REST | `GET sell/inventory/v1/inventory_item` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/inventory_item/methods/getInventoryItems) |
| [List Inventory Locations](actions/list-inventory-locations.md) | REST | `GET sell/inventory/v1/location` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/location/methods/getInventoryLocations) |
| [List Item Aspects for Category](actions/list-item-aspects-for-category.md) | REST | `GET commerce/taxonomy/v1/category_tree/0/get_item_aspects_for_category` | [docs](https://developer.ebay.com/api-docs/commerce/taxonomy/resources/category_tree/methods/getItemAspectsForCategory) |
| [List Opted-In Programs](actions/list-opted-in-programs.md) | REST | `GET sell/account/v1/program/get_opted_in_programs` | [docs](https://developer.ebay.com/api-docs/sell/account/resources/program/methods/getOptedInPrograms) |
| [List Orders](actions/list-orders.md) | REST | `GET sell/fulfillment/v1/order` | [docs](https://developer.ebay.com/api-docs/sell/fulfillment/resources/order/methods/getOrders) |
| [List Payout Transactions](actions/list-payout-transactions.md) | Sell Finances | `GET /transaction` | [docs](https://developer.ebay.com/develop/api/sell/finances_api/transaction/getTransactions) |
| [List Payouts](actions/list-payouts.md) | Sell Finances | `GET /payout` | [docs](https://developer.ebay.com/develop/api/sell/finances_api/payout/getPayouts) |
| [List Seller Items](actions/list-seller-items.md) | REST eBay XML | `POST` | [docs](https://developer.ebay.com/devzone/xml/docs/reference/ebay/GetSellerList.html) |
| [List Seller Items_v2](actions/list-seller-items-v2.md) | REST eBay XML | `POST` | [docs](https://developer.ebay.com/devzone/xml/docs/reference/ebay/GetSellerList.html) |
| [List Selling Policies](actions/list-selling-policies.md) | REST | `GET sell/account/v1/:policy/` | [docs](https://developer.ebay.com/api-docs/sell/account/resources/custom_policy/methods/getCustomPolicies) |
| [Opt-In to Program](actions/opt-in-to-program.md) | REST | `POST sell/account/v1/program/opt_in` | [docs](https://developer.ebay.com/api-docs/sell/account/resources/program/methods/optInToProgram) |
| [Opt-Out of Program](actions/opt-out-of-program.md) | REST | `POST sell/account/v1/program/opt_out` | [docs](https://developer.ebay.com/api-docs/sell/account/resources/program/methods/optOutOfProgram) |
| [Publish Offer](actions/publish-offer.md) | REST | `POST sell/inventory/v1/offer/:offerId/publish` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/publishOffer) |
| [Revise Inventory Status](actions/revise-inventory-status.md) | REST eBay XML | `POST` | [docs](https://developer.ebay.com/devzone/xml/docs/reference/ebay/ReviseInventoryStatus.html) |
| [Update Offer](actions/update-offer.md) | REST | `PUT sell/inventory/v1/offer/:offerId` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/updateOffer) |
| [Update - Price and Quantity](actions/update-price-and-quantity.md) | REST | `POST sell/inventory/v1/bulk_update_price_quantity` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/updateOffer) |
| [Withdraw Offer](actions/withdraw-offer.md) | REST | `POST sell/inventory/v1/offer/:offerId/withdraw` | [docs](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/withdrawOffer) |
