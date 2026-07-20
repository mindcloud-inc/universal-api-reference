# <img src="https://images.mindcloud.co/apps/icons/evoliz_1774017719152.png" alt="Evoliz logo" width="28" height="28"> Evoliz: Universal API

Manage clients, quotes, invoices, and sales documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/evoliz/latest
- **Category:** Commerce / Accounting
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.evoliz.com
- **Vendor API docs:** https://evoliz.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Article](actions/get-article.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/get-article?connectionId=$CONNECTION_ID&articleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Get Article](actions/get-article.md) | GET | Retrieves an article from Evoliz. |
| [List Articles](actions/list-articles.md) | GET | Retrieves articles from Evoliz. |
| [Update Article](actions/update-article.md) | PUT | Updates an existing article in Evoliz. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Evoliz. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Evoliz. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Evoliz. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Evoliz. |

### Client Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Contact](actions/create-client-contact.md) | POST | Creates a new client contact in Evoliz. |
| [List Client Contacts](actions/list-client-contacts.md) | GET | Retrieves client contacts from Evoliz. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Evoliz. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Evoliz. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Evoliz. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Evoliz. |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST | Creates a new quote in Evoliz. |
| [Get Quote](actions/get-quote.md) | GET | Retrieves a quote from Evoliz. |
| [List Quotes](actions/list-quotes.md) | GET | Retrieves quotes from Evoliz. |
| [Send Quote](actions/send-quote.md) | PUT | Sends a quote by email from Evoliz. |
| [Update Quote](actions/update-quote.md) | PUT | Updates an existing quote in Evoliz. |

### Sale Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Sale Order](actions/create-sale-order.md) | POST | Creates a new sale order in Evoliz. |
| [Get Sale Order](actions/get-sale-order.md) | GET | Retrieves a sale order from Evoliz. |
| [List Sale Orders](actions/list-sale-orders.md) | GET | Retrieves sale orders from Evoliz. |
| [Update Sale Order](actions/update-sale-order.md) | PUT | Updates an existing sale order in Evoliz. |

