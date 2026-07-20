# <img src="https://images.mindcloud.co/apps/icons/ontraport_1773241701143.png" alt="Ontraport logo" width="28" height="28"> Ontraport: Universal API

Manage contacts, campaigns, payments, and messaging in Ontraport

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ontraport/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ontraport.com/
- **Vendor API docs:** https://api.ontraport.com/doc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Contact Object Meta](actions/retrieve-contact-object-meta.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-contact-object-meta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Ontraport. |
| [Retrieve Contact Collection Info](actions/retrieve-contact-collection-info.md) | GET | Retrieves collection info for contacts in Ontraport. |
| [Retrieve Contact Object Meta](actions/retrieve-contact-object-meta.md) | GET | Retrieves metadata for contact objects in Ontraport. |
| [Retrieve Specific Contact](actions/retrieve-specific-contact.md) | GET | Retrieves a specific contact from Ontraport. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves a list of messages from Ontraport. |
| [Retrieve Message Collection Info](actions/retrieve-message-collection-info.md) | GET | Retrieves collection info for messages in Ontraport. |
| [Retrieve Message Meta](actions/retrieve-message-meta.md) | GET | Retrieves metadata for messages in Ontraport. |
| [Retrieve Specific Message](actions/retrieve-specific-message.md) | GET | Retrieves a specific message from Ontraport. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Ontraport. |
| [Retrieve Product Collection Info](actions/retrieve-product-collection-info.md) | GET | Retrieves collection info for products in Ontraport. |
| [Retrieve Product Object Meta](actions/retrieve-product-object-meta.md) | GET | Retrieves metadata for product objects in Ontraport. |
| [Retrieve Specific Product](actions/retrieve-specific-product.md) | GET | Retrieves a specific product from Ontraport. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves a list of tags from Ontraport. |
| [Retrieve Specific Tag](actions/retrieve-specific-tag.md) | GET | Retrieves a specific tag from Ontraport. |
| [Retrieve Tag Collection Info](actions/retrieve-tag-collection-info.md) | GET | Retrieves collection info for tags in Ontraport. |
| [Retrieve Tag Object Meta](actions/retrieve-tag-object-meta.md) | GET | Retrieves metadata for tag objects in Ontraport. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Ontraport. |
| [Retrieve Specific Task](actions/retrieve-specific-task.md) | GET | Retrieves a specific task from Ontraport. |
| [Retrieve Task Collection Info](actions/retrieve-task-collection-info.md) | GET | Retrieves collection info for tasks in Ontraport. |
| [Retrieve Task Object Meta](actions/retrieve-task-object-meta.md) | GET | Retrieves metadata for task objects in Ontraport. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves a list of transactions from Ontraport. |
| [Retrieve Single Transaction](actions/retrieve-single-transaction.md) | GET | Retrieves a single transaction from Ontraport. |
| [Retrieve Transaction Collection Info](actions/retrieve-transaction-collection-info.md) | GET | Retrieves collection info for transactions in Ontraport. |
| [Retrieve Transaction Object Meta](actions/retrieve-transaction-object-meta.md) | GET | Retrieves metadata for transaction objects in Ontraport. |

