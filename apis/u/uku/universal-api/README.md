# <img src="https://images.mindcloud.co/apps/icons/favicon_1774986524083.png" alt="Uku logo" width="28" height="28"> Uku: Universal API

Manage clients, tasks, time entries, contracts, and invoices with Uku

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uku/latest
- **Category:** Productivity / Project Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getuku.com/
- **Vendor API docs:** https://app.getuku.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Uku. |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves contracts from Uku. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Field](actions/get-client-field.md) | GET | Retrieves a client field from Uku. |
| [List Client Fields](actions/list-client-fields.md) | GET | Retrieves client fields from Uku. |
| [List Product Fields](actions/list-product-fields.md) | GET | Retrieves product fields from Uku. |
| [List Task Fields](actions/list-task-fields.md) | GET | Retrieves task fields from Uku. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Uku. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Uku. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Uku. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice Seller](actions/get-invoice-seller.md) | GET | Retrieves an invoice seller from Uku. |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from Uku. |
| [List Invoice Sellers](actions/list-invoice-sellers.md) | GET | Retrieves invoice sellers from Uku. |
| [List Members](actions/list-members.md) | GET | Retrieves members from Uku. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Group](actions/get-client-group.md) | GET | Retrieves a client group from Uku. |
| [Get Member Group](actions/get-member-group.md) | GET | Retrieves a member group from Uku. |
| [List Client Groups](actions/list-client-groups.md) | GET | Retrieves client groups from Uku. |
| [List Member Groups](actions/list-member-groups.md) | GET | Retrieves member groups from Uku. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from Uku. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Topic](actions/get-topic.md) | GET | Retrieves a topic from Uku. |
| [List Topics](actions/list-topics.md) | GET | Retrieves topics from Uku. |

