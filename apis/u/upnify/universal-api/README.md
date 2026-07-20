# <img src="https://images.mindcloud.co/apps/icons/images-1_1774285893546.jpeg" alt="Upnify logo" width="28" height="28"> Upnify: Universal API

Upnify CRM REST API wrapper for prospects, clients, opportunities, sales, companies, catalogs, and reports.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/upnify/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://upnify.com/
- **Vendor API docs:** https://desarrollo.upnify.com/api-rest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Upnify. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Upnify. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Upnify. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Upnify. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Upnify. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Upnify. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Upnify. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Upnify. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Upnify. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Upnify. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Company Contacts](actions/list-company-contacts.md) | GET | Retrieves contacts for a company in Upnify. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE | Deletes an existing opportunity from Upnify. |
| [Get Opportunity](actions/get-opportunity.md) | GET | Retrieves an opportunity from Upnify. |
| [List Client Opportunities](actions/list-client-opportunities.md) | GET | Retrieves opportunities for a client in Upnify. |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves opportunities from Upnify. |
| [List Prospect Opportunities](actions/list-prospect-opportunities.md) | GET | Retrieves opportunities for a prospect in Upnify. |
| [Update Opportunity](actions/update-opportunity.md) | PUT | Updates an existing opportunity in Upnify. |

### Opportunity Estimate

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Estimates](actions/list-sales-estimates.md) | GET | Retrieves sales estimates from Upnify. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Sale Payments](actions/list-sale-payments.md) | GET | Retrieves payments for a sale in Upnify. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Upnify. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Upnify. |
| [List Opportunity Products](actions/list-opportunity-products.md) | GET | Retrieves products for an opportunity in Upnify. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Upnify. |
| [List Sale Products](actions/list-sale-products.md) | GET | Retrieves products for a sale in Upnify. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Upnify. |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Create Prospect](actions/create-prospect.md) | POST | Creates a new prospect in Upnify. |
| [Delete Prospect](actions/delete-prospect.md) | DELETE | Deletes an existing prospect from Upnify. |
| [Get Prospect](actions/get-prospect.md) | GET | Retrieves a prospect from Upnify. |
| [List Prospects](actions/list-prospects.md) | GET | Retrieves prospects from Upnify. |
| [Update Prospect](actions/update-prospect.md) | PUT | Updates an existing prospect in Upnify. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Create Sale](actions/create-sale.md) | POST | Creates a new sale in Upnify. |
| [Delete Sale](actions/delete-sale.md) | DELETE | Deletes an existing sale from Upnify. |
| [Get Sale](actions/get-sale.md) | GET | Retrieves a sale from Upnify. |
| [List Sales](actions/list-sales.md) | GET | Retrieves sales from Upnify. |
| [Update Sale](actions/update-sale.md) | PUT | Updates an existing sale in Upnify. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Upnify. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Upnify. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Upnify. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Upnify. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Upnify. |

