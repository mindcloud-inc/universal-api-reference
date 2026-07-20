# <img src="https://images.mindcloud.co/apps/icons/favicon-developers-farmbrite-com-48x48_1776885454960.png" alt="Farmbrite logo" width="28" height="28"> Farmbrite: Universal API

Farmbrite is farm management software for livestock, crops, inventory, orders, tasks, and day-to-day farm operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/farmbrite/latest
- **Category:** Commerce / ERP
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://farmbrite.com
- **Vendor API docs:** https://developers.farmbrite.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Animals

| Action | Method | Description |
| --- | --- | --- |
| [Create animal](actions/create-animal.md) | POST | Creates a new animal in Farmbrite. |
| [Delete animal](actions/delete-animal.md) | DELETE | Deletes an existing animal from Farmbrite. |
| [List animals](actions/list-animals.md) | GET | Retrieves a list of animals from Farmbrite. |
| [Retrieve animal](actions/retrieve-animal.md) | GET | Retrieves a specific animal from Farmbrite. |
| [Update animal](actions/update-animal.md) | PUT | Updates an existing animal in Farmbrite. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create contact](actions/create-contact.md) | POST | Creates a new contact in Farmbrite. |
| [Delete contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Farmbrite. |
| [List contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Farmbrite. |
| [Retrieve contact](actions/retrieve-contact.md) | GET | Retrieves a specific contact from Farmbrite. |
| [Update contact](actions/update-contact.md) | PUT | Updates an existing contact in Farmbrite. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create order](actions/create-order.md) | POST | Creates a new order in Farmbrite. |
| [Delete order](actions/delete-order.md) | DELETE | Deletes an existing order from Farmbrite. |
| [List orders](actions/list-orders.md) | GET | Retrieves a list of orders from Farmbrite. |
| [Retrieve order](actions/retrieve-order.md) | GET | Retrieves a specific order from Farmbrite. |

### Plots

| Action | Method | Description |
| --- | --- | --- |
| [Create plot](actions/create-plot.md) | POST | Creates a new plot in Farmbrite. |
| [Delete plot](actions/delete-plot.md) | DELETE | Deletes an existing plot from Farmbrite. |
| [List plots](actions/list-plots.md) | GET | Retrieves a list of plots from Farmbrite. |
| [Retrieve plot](actions/retrieve-plot.md) | GET | Retrieves a specific plot from Farmbrite. |
| [Update plot](actions/update-plot.md) | PUT | Updates an existing plot in Farmbrite. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create product](actions/create-product.md) | POST | Creates a new product in Farmbrite. |
| [Delete product](actions/delete-product.md) | DELETE | Deletes an existing product from Farmbrite. |
| [List products](actions/list-products.md) | GET | Retrieves a list of products from Farmbrite. |
| [Retrieve product](actions/retrieve-product.md) | GET | Retrieves a specific product from Farmbrite. |
| [Update product](actions/update-product.md) | PUT | Updates an existing product in Farmbrite. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create task](actions/create-task.md) | POST | Creates a new task in Farmbrite. |
| [Delete task](actions/delete-task.md) | DELETE | Deletes an existing task from Farmbrite. |
| [List tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Farmbrite. |
| [Retrieve task](actions/retrieve-task.md) | GET | Retrieves a specific task from Farmbrite. |
| [Update task](actions/update-task.md) | PUT | Updates an existing task in Farmbrite. |

### Tools

| Action | Method | Description |
| --- | --- | --- |
| [Create tool](actions/create-tool.md) | POST | Creates a new tool in Farmbrite. |
| [Delete tool](actions/delete-tool.md) | DELETE | Deletes an existing tool from Farmbrite. |
| [List tools](actions/list-tools.md) | GET | Retrieves a list of tools from Farmbrite. |
| [Retrieve tool](actions/retrieve-tool.md) | GET | Retrieves a specific tool from Farmbrite. |
| [Update tool](actions/update-tool.md) | PUT | Updates an existing tool in Farmbrite. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create transaction](actions/create-transaction.md) | POST | Creates a new transaction in Farmbrite. |
| [Delete transaction](actions/delete-transaction.md) | DELETE | Deletes an existing transaction from Farmbrite. |
| [List transactions](actions/list-transactions.md) | GET | Retrieves a list of transactions from Farmbrite. |
| [Retrieve transaction](actions/retrieve-transaction.md) | GET | Retrieves a specific transaction from Farmbrite. |
| [Update transaction](actions/update-transaction.md) | PUT | Updates an existing transaction in Farmbrite. |

