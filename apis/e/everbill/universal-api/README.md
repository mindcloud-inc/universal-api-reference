# <img src="https://images.mindcloud.co/apps/icons/id-gi-vz-gku-k-logos_1777499499813.png" alt="Everbill logo" width="28" height="28"> Everbill: Universal API

Manage invoices, expenses, accounting documents, and business contacts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/everbill/latest
- **Category:** Commerce / Accounting
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.everbill.com/
- **Vendor API docs:** https://api.everbill.eu/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Articles](actions/list-articles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everbill/latest/actions/list-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Sign In](actions/sign-in.md) | GET | Retrieves an access token from Everbill. |

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST | Creates a new article in Everbill. |
| [Get Article](actions/get-article.md) | GET | Retrieves an article from Everbill. |
| [List Articles](actions/list-articles.md) | GET | Retrieves articles from Everbill. |
| [Update Article](actions/update-article.md) | PUT | Updates an existing article in Everbill. |

### Article Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Article Category](actions/create-article-category.md) | POST | Creates a new article category in Everbill. |
| [List Article Categories](actions/list-article-categories.md) | GET | Retrieves article categories from Everbill. |

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [Add Bill Item](actions/add-bill-item.md) | POST | Creates a new bill item in Everbill. |
| [Add Bill Transaction](actions/add-bill-transaction.md) | POST | Creates a new bill transaction in Everbill. |
| [Create Bill](actions/create-bill.md) | POST | Creates a new bill in Everbill. |
| [Get Bill](actions/get-bill.md) | GET | Retrieves a bill from Everbill. |
| [List Bills](actions/list-bills.md) | GET | Retrieves bills from Everbill. |
| [Update Bill](actions/update-bill.md) | PUT | Updates an existing bill in Everbill. |

### Cost Unit

| Action | Method | Description |
| --- | --- | --- |
| [Create Cost Unit](actions/create-cost-unit.md) | POST | Creates a new cost unit in Everbill. |
| [Get Cost Unit](actions/get-cost-unit.md) | GET | Retrieves a cost unit from Everbill. |
| [List Cost Units](actions/list-cost-units.md) | GET | Retrieves cost units from Everbill. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Everbill. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Everbill. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Everbill. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Everbill. |

### Distributor

| Action | Method | Description |
| --- | --- | --- |
| [Create Distributor](actions/create-distributor.md) | POST | Creates a new distributor in Everbill. |
| [Get Distributor](actions/get-distributor.md) | GET | Retrieves a distributor from Everbill. |
| [List Distributors](actions/list-distributors.md) | GET | Retrieves distributors from Everbill. |
| [Update Distributor](actions/update-distributor.md) | PUT | Updates an existing distributor in Everbill. |

### Document Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Get Document PDF](actions/get-document-pdf.md) | GET | Retrieves a document PDF from Everbill. |

### Incoming Bill

| Action | Method | Description |
| --- | --- | --- |
| [Create Incoming Bill](actions/create-incoming-bill.md) | POST | Creates a new incoming bill in Everbill. |
| [Get Incoming Bill](actions/get-incoming-bill.md) | GET | Retrieves an incoming bill from Everbill. |
| [List Incoming Bills](actions/list-incoming-bills.md) | GET | Retrieves incoming bills from Everbill. |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Add Offer Item](actions/add-offer-item.md) | POST | Creates a new offer item in Everbill. |
| [Create Offer](actions/create-offer.md) | POST | Creates a new offer in Everbill. |
| [Get Offer](actions/get-offer.md) | GET | Retrieves an offer from Everbill. |
| [List Offers](actions/list-offers.md) | GET | Retrieves offers from Everbill. |
| [Update Offer](actions/update-offer.md) | PUT | Updates an existing offer in Everbill. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Add Order Item](actions/add-order-item.md) | POST | Creates a new order item in Everbill. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Everbill. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Everbill. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Everbill. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Everbill. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Everbill. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Everbill. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Everbill. |

