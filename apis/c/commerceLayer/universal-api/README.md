# <img src="https://images.mindcloud.co/apps/icons/commerce-layer_1774880169141.png" alt="Commerce Layer logo" width="28" height="28"> Commerce Layer: Universal API

Manage markets, inventory, orders, pricing, and promotions across channels

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/commerceLayer/latest
- **Category:** Commerce
- **Actions:** 59
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://commercelayer.io
- **Vendor API docs:** https://docs.commercelayer.io/core-api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Markets](actions/list-markets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-markets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (59)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | POST |  |
| [Delete Address](actions/delete-address.md) | DELETE |  |
| [Get Address](actions/get-address.md) | GET |  |
| [List Addresses](actions/list-addresses.md) | GET |  |
| [Update Address](actions/update-address.md) | PUT |  |

### Avalara Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Avalara Account](actions/create-avalara-account.md) | POST |  |
| [List Avalara Accounts](actions/list-avalara-accounts.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Group](actions/create-customer-group.md) | POST |  |
| [Delete Customer Group](actions/delete-customer-group.md) | DELETE |  |
| [Get Customer Group](actions/get-customer-group.md) | GET |  |
| [List Customer Groups](actions/list-customer-groups.md) | GET |  |
| [Update Customer Group](actions/update-customer-group.md) | PUT |  |

### Inventory Model

| Action | Method | Description |
| --- | --- | --- |
| [Create Inventory Model](actions/create-inventory-model.md) | POST |  |
| [Delete Inventory Model](actions/delete-inventory-model.md) | DELETE |  |
| [Get Inventory Model](actions/get-inventory-model.md) | GET |  |
| [List Inventory Models](actions/list-inventory-models.md) | GET |  |
| [Update Inventory Model](actions/update-inventory-model.md) | PUT |  |

### Manual Tax Calculator

| Action | Method | Description |
| --- | --- | --- |
| [Create Manual Tax Calculator](actions/create-manual-tax-calculator.md) | POST |  |
| [Delete Manual Tax Calculator](actions/delete-manual-tax-calculator.md) | DELETE |  |
| [Get Manual Tax Calculator](actions/get-manual-tax-calculator.md) | GET |  |
| [List Manual Tax Calculators](actions/list-manual-tax-calculators.md) | GET |  |
| [Update Manual Tax Calculator](actions/update-manual-tax-calculator.md) | PUT |  |

### Market

| Action | Method | Description |
| --- | --- | --- |
| [Create Market](actions/create-market.md) | POST |  |
| [Delete Market](actions/delete-market.md) | DELETE |  |
| [Get Market](actions/get-market.md) | GET |  |
| [List Markets](actions/list-markets.md) | GET |  |
| [Update Market](actions/update-market.md) | PUT |  |

### Merchant

| Action | Method | Description |
| --- | --- | --- |
| [Create Merchant](actions/create-merchant.md) | POST |  |
| [Delete Merchant](actions/delete-merchant.md) | DELETE |  |
| [Get Merchant](actions/get-merchant.md) | GET |  |
| [List Merchants](actions/list-merchants.md) | GET |  |
| [Update Merchant](actions/update-merchant.md) | PUT |  |

### Price List

| Action | Method | Description |
| --- | --- | --- |
| [Create Price List](actions/create-price-list.md) | POST |  |
| [Delete Price List](actions/delete-price-list.md) | DELETE |  |
| [Get Price List](actions/get-price-list.md) | GET |  |
| [List Price Lists](actions/list-price-lists.md) | GET |  |
| [Update Price List](actions/update-price-list.md) | PUT |  |

### Shipping Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipping Category](actions/create-shipping-category.md) | POST |  |
| [Delete Shipping Category](actions/delete-shipping-category.md) | DELETE |  |
| [Get Shipping Category](actions/get-shipping-category.md) | GET |  |
| [List Shipping Categories](actions/list-shipping-categories.md) | GET |  |
| [Update Shipping Category](actions/update-shipping-category.md) | PUT |  |

### Sku

| Action | Method | Description |
| --- | --- | --- |
| [Create SKU](actions/create-sku.md) | POST |  |

### Stock Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Stock Location](actions/create-stock-location.md) | POST |  |
| [Delete Stock Location](actions/delete-stock-location.md) | DELETE |  |
| [Get Stock Location](actions/get-stock-location.md) | GET |  |
| [List Stock Locations](actions/list-stock-locations.md) | GET |  |
| [Update Stock Location](actions/update-stock-location.md) | PUT |  |

### Tax Calculator

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Calculators](actions/list-tax-calculators.md) | GET |  |

### Tax Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Tax Category](actions/create-tax-category.md) | POST |  |
| [Delete Tax Category](actions/delete-tax-category.md) | DELETE |  |
| [Get Tax Category](actions/get-tax-category.md) | GET |  |
| [List Tax Categories](actions/list-tax-categories.md) | GET |  |
| [Update Tax Category](actions/update-tax-category.md) | PUT |  |

### Tax Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Tax Rule](actions/create-tax-rule.md) | POST |  |
| [Delete Tax Rule](actions/delete-tax-rule.md) | DELETE |  |
| [Get Tax Rule](actions/get-tax-rule.md) | GET |  |
| [List Tax Rules](actions/list-tax-rules.md) | GET |  |
| [Update Tax Rule](actions/update-tax-rule.md) | PUT |  |

