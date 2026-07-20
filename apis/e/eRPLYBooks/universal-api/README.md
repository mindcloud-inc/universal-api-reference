# <img src="https://images.mindcloud.co/apps/icons/e-rplybooks_1776093356637.png" alt="ERPLY Books logo" width="28" height="28"> ERPLY Books: Universal API

ERPLY Books lets you connect your ERPLY account to list retail master data, customers, company settings, sales documents, inventory references, and supporting accounting records through the classic ERPLY API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eRPLYBooks/latest
- **Category:** Commerce / ERP
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://erply.com
- **Vendor API docs:** https://learn-api.erply.com/requests

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Info](actions/get-company-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-company-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Get Address Types](actions/get-address-types.md) | GET | Retrieves address types from ERPLY Books. |
| [Get Addresses](actions/get-addresses.md) | GET | Retrieves address records from ERPLY Books. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaigns](actions/get-campaigns.md) | GET | Retrieves campaign records from ERPLY Books. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Categories](actions/get-product-categories.md) | GET | Retrieves product categories from ERPLY Books. |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Info](actions/get-company-info.md) | GET | Retrieves company information from ERPLY Books. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET | Authenticates an ERPLY Books connection and returns session details. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customers](actions/get-customers.md) | GET | Retrieves customer records from ERPLY Books. |
| [Get Default Customer](actions/get-default-customer.md) | GET | Retrieves the default customer from ERPLY Books. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Documents](actions/get-purchase-documents.md) | GET | Retrieves purchase documents from ERPLY Books. |
| [Get Sales Documents](actions/get-sales-documents.md) | GET | Retrieves sales documents from ERPLY Books. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employees](actions/get-employees.md) | GET | Retrieves employee records from ERPLY Books. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Groups](actions/get-customer-groups.md) | GET | Retrieves customer groups from ERPLY Books. |
| [Get Product Groups](actions/get-product-groups.md) | GET | Retrieves product groups from ERPLY Books. |

### Inventory Levels

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Stock](actions/get-product-stock.md) | GET | Retrieves product stock levels from ERPLY Books. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Types](actions/get-payment-types.md) | GET | Retrieves payment types from ERPLY Books. |

### Price Books

| Action | Method | Description |
| --- | --- | --- |
| [Get Price Lists](actions/get-price-lists.md) | GET | Retrieves price lists from ERPLY Books. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Products](actions/get-products.md) | GET | Retrieves product records from ERPLY Books. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Projects](actions/get-projects.md) | GET | Retrieves project records from ERPLY Books. |

### Reference Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Brands](actions/get-brands.md) | GET | Retrieves brand records from ERPLY Books. |
| [Get Configuration Parameters](actions/get-conf-parameters.md) | GET | Retrieves configuration parameters from ERPLY Books. |
| [Get Countries](actions/get-countries.md) | GET | Retrieves country records from ERPLY Books. |
| [Get Currencies](actions/get-currencies.md) | GET | Retrieves currency records from ERPLY Books. |
| [Get Points of Sale](actions/get-points-of-sale.md) | GET | Retrieves points of sale from ERPLY Books. |
| [Get Product Priority Groups](actions/get-product-priority-groups.md) | GET | Retrieves product priority groups from ERPLY Books. |
| [Get Product Units](actions/get-product-units.md) | GET | Retrieves product units from ERPLY Books. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Get Services](actions/get-services.md) | GET | Retrieves service records from ERPLY Books. |

### Tax Rates

| Action | Method | Description |
| --- | --- | --- |
| [Get VAT Rates](actions/get-vat-rates.md) | GET | Retrieves VAT rates from ERPLY Books. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Get Suppliers](actions/get-suppliers.md) | GET | Retrieves supplier records from ERPLY Books. |

### Warehouses

| Action | Method | Description |
| --- | --- | --- |
| [Get Allowed Warehouses](actions/get-allowed-warehouses.md) | GET | Retrieves allowed warehouses from ERPLY Books. |
| [Get Warehouses](actions/get-warehouses.md) | GET | Retrieves warehouse records from ERPLY Books. |

