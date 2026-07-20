# <img src="https://images.mindcloud.co/apps/icons/lightspeed-retail-x_1774886544038.jpeg" alt="Lightspeed Retail POS (X-Series) logo" width="28" height="28"> Lightspeed Retail POS (X-Series): Universal API

Manage products, customers, sales, suppliers, and stores

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lightspeedRetailPOSXSeries/latest
- **Category:** Commerce
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lightspeedhq.com/pos/retail/
- **Vendor API docs:** https://x-series-api.lightspeedhq.com/docs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Retailer](actions/get-retailer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-retailer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Retailer](actions/get-retailer.md) | GET | Retrieves retailer information from Lightspeed Retail POS (X-Series). |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Lightspeed Retail POS (X-Series). |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Lightspeed Retail POS (X-Series). |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Lightspeed Retail POS (X-Series). |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Lightspeed Retail POS (X-Series). |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Outlet](actions/get-outlet.md) | GET | Retrieves an outlet from Lightspeed Retail POS (X-Series). |
| [List Outlets](actions/list-outlets.md) | GET | Retrieves outlets from Lightspeed Retail POS (X-Series). |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Lightspeed Retail POS (X-Series). |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Lightspeed Retail POS (X-Series). |
| [List Products](actions/list-products.md) | GET | Retrieves products from Lightspeed Retail POS (X-Series). |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Sales](actions/list-sales.md) | GET | Retrieves sales from Lightspeed Retail POS (X-Series). |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Register](actions/get-register.md) | GET | Retrieves a register from Lightspeed Retail POS (X-Series). |
| [List Registers](actions/list-registers.md) | GET | Retrieves registers from Lightspeed Retail POS (X-Series). |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Lightspeed Retail POS (X-Series). |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Lightspeed Retail POS (X-Series). |
| [List Users](actions/list-users.md) | GET | Retrieves users from Lightspeed Retail POS (X-Series). |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST | Creates a new supplier in Lightspeed Retail POS (X-Series). |
| [Get Supplier](actions/get-supplier.md) | GET | Retrieves a supplier from Lightspeed Retail POS (X-Series). |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Lightspeed Retail POS (X-Series). |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Lightspeed Retail POS (X-Series). |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Lightspeed Retail POS (X-Series). |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Lightspeed Retail POS (X-Series). |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Lightspeed Retail POS (X-Series). |

