# <img src="https://images.mindcloud.co/apps/icons/zydon_1775164885712.png" alt="Zydon logo" width="28" height="28"> Zydon: Universal API

Access Zydon's sales API for partners, orders, products, pricing, categories, sellers, companies, stock, and financial data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zydon/latest
- **Category:** Commerce
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zydon.com.br
- **Vendor API docs:** https://docs.zydon.com.br/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Companies](actions/list-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zydon/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Get Brand](actions/get-brand.md) | GET | Retrieves brand details from Zydon. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brand records from Zydon. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves category details from Zydon. |
| [List Categories](actions/list-categories.md) | GET | Retrieves category records from Zydon. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from Zydon. |
| [List Companies](actions/list-companies.md) | GET | Retrieves company records from Zydon. |

### Financial

| Action | Method | Description |
| --- | --- | --- |
| [List Financials](actions/list-financials.md) | GET | Retrieves financial records from Zydon. |
| [List Financials By Order](actions/list-financials-by-order.md) | GET | Retrieves financial records for an order from Zydon. |

### Measure Unit

| Action | Method | Description |
| --- | --- | --- |
| [Get Measure Unit](actions/get-measure-unit.md) | GET | Retrieves measure unit details from Zydon. |
| [List Measure Units](actions/list-measure-units.md) | GET | Retrieves measure units from Zydon. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves order details from Zydon. |
| [List Orders](actions/list-orders.md) | GET | Retrieves order records from Zydon. |

### Partner

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner](actions/get-partner.md) | GET | Retrieves partner details from Zydon. |
| [List Partners](actions/list-partners.md) | GET | Retrieves partner records from Zydon. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Method](actions/get-payment-method.md) | GET | Retrieves payment method details from Zydon. |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from Zydon. |

### Price Table

| Action | Method | Description |
| --- | --- | --- |
| [Get Price Table](actions/get-price-table.md) | GET | Retrieves price table details from Zydon. |
| [List Price Tables](actions/list-price-tables.md) | GET | Retrieves price tables from Zydon. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves product details from Zydon. |
| [List Products](actions/list-products.md) | GET | Retrieves product records from Zydon. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves profile details from Zydon. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves profile records from Zydon. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Get Sale](actions/get-sale.md) | GET | Retrieves sale details from Zydon. |
| [List Sales](actions/list-sales.md) | GET | Retrieves sales records from Zydon. |

### Seller

| Action | Method | Description |
| --- | --- | --- |
| [Get Seller](actions/get-seller.md) | GET | Retrieves seller details from Zydon. |
| [List Sellers](actions/list-sellers.md) | GET | Retrieves seller records from Zydon. |

### Variation

| Action | Method | Description |
| --- | --- | --- |
| [Get Variation](actions/get-variation.md) | GET | Retrieves variation details from Zydon. |
| [List Variations](actions/list-variations.md) | GET | Retrieves variation records from Zydon. |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [Get Warehouse](actions/get-warehouse.md) | GET | Retrieves warehouse details from Zydon. |
| [List Warehouses](actions/list-warehouses.md) | GET | Retrieves warehouse records from Zydon. |

