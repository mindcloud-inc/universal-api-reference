# <img src="https://images.mindcloud.co/apps/icons/0x0_1781889316082.png" alt="e-Boekhouden.nl logo" width="28" height="28"> e-Boekhouden.nl: Universal API

Dutch bookkeeping and accounting platform for invoices, relations, ledgers, and financial administration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/e-boekhouden-nl/latest
- **Category:** Commerce / ERP
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.e-boekhouden.nl/
- **Vendor API docs:** https://api.e-boekhouden.nl/swagger/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Relations](actions/list-relations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/list-relations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Administrations

| Action | Method | Description |
| --- | --- | --- |
| [List Administrations](actions/list-administrations.md) | GET | Retrieves administrations from e-Boekhouden.nl. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Relations](actions/list-relations.md) | GET | Retrieves relations from e-Boekhouden.nl. |

### Cost Center

| Action | Method | Description |
| --- | --- | --- |
| [Create Cost Center](actions/create-cost-center.md) | POST | Creates a new cost center in e-Boekhouden.nl. |
| [Delete Cost Center](actions/delete-cost-center.md) | DELETE | Deletes a cost center from e-Boekhouden.nl. |
| [Get Cost Center](actions/get-cost-center.md) | GET | Retrieves a cost center from e-Boekhouden.nl. |
| [Update Cost Center](actions/update-cost-center.md) | PUT | Updates a cost center in e-Boekhouden.nl. |

### Cost Centers

| Action | Method | Description |
| --- | --- | --- |
| [List Cost Centers](actions/list-cost-centers.md) | GET | Retrieves cost centers from e-Boekhouden.nl. |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves email templates from e-Boekhouden.nl. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in e-Boekhouden.nl. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from e-Boekhouden.nl. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Templates](actions/list-invoice-templates.md) | GET | Retrieves invoice templates from e-Boekhouden.nl. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from e-Boekhouden.nl. |

### Ledger

| Action | Method | Description |
| --- | --- | --- |
| [Create Ledger](actions/create-ledger.md) | POST | Creates a new ledger in e-Boekhouden.nl. |
| [Get Ledger](actions/get-ledger.md) | GET | Retrieves a ledger from e-Boekhouden.nl. |
| [Update Ledger](actions/update-ledger.md) | PUT | Updates a ledger in e-Boekhouden.nl. |

### Ledger Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Ledger Balance](actions/get-ledger-balance.md) | GET | Retrieves a ledger balance from e-Boekhouden.nl. |

### Ledgers

| Action | Method | Description |
| --- | --- | --- |
| [List Ledgers](actions/list-ledgers.md) | GET | Retrieves ledgers from e-Boekhouden.nl. |

### Linked Administrations

| Action | Method | Description |
| --- | --- | --- |
| [List Linked Administrations](actions/list-linked-administrations.md) | GET | Retrieves linked administrations from e-Boekhouden.nl. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST | Creates a new member in e-Boekhouden.nl. |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from e-Boekhouden.nl. |
| [Update Member](actions/update-member.md) | PUT | Updates a member in e-Boekhouden.nl. |

### Members

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves members from e-Boekhouden.nl for clubs or associations. |

### Mutation

| Action | Method | Description |
| --- | --- | --- |
| [Create Mutation](actions/create-mutation.md) | POST | Creates a new mutation in e-Boekhouden.nl. |
| [Get Mutation](actions/get-mutation.md) | GET | Retrieves a mutation from e-Boekhouden.nl. |

### Mutations

| Action | Method | Description |
| --- | --- | --- |
| [List Mutations](actions/list-mutations.md) | GET | Retrieves mutations from e-Boekhouden.nl. |

### Outstanding Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Outstanding Invoices](actions/list-outstanding-invoices.md) | GET | Retrieves outstanding invoices from e-Boekhouden.nl. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in e-Boekhouden.nl. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes a product from e-Boekhouden.nl. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from e-Boekhouden.nl. |
| [Update Product](actions/update-product.md) | PUT | Updates a product in e-Boekhouden.nl. |

### Product Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Product Groups](actions/list-product-groups.md) | GET | Retrieves product groups from e-Boekhouden.nl. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from e-Boekhouden.nl. |

### Relation

| Action | Method | Description |
| --- | --- | --- |
| [Create Relation](actions/create-relation.md) | POST | Creates a new relation in e-Boekhouden.nl. |
| [Get Relation](actions/get-relation.md) | GET | Retrieves a relation from e-Boekhouden.nl. |
| [Update Relation](actions/update-relation.md) | PUT | Updates a relation in e-Boekhouden.nl. |

### Units

| Action | Method | Description |
| --- | --- | --- |
| [List Units](actions/list-units.md) | GET | Retrieves units from e-Boekhouden.nl. |

