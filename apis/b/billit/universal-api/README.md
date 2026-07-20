# <img src="https://images.mindcloud.co/apps/icons/billit_1773938218942.png" alt="Billit logo" width="28" height="28"> Billit: Universal API

Create and manage Billit accounting data with PartyID plus API key authentication for sandbox testing.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/billit/latest
- **Category:** Commerce / Accounting
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.billit.be
- **Vendor API docs:** https://docs.billit.be/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Account Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves account information for the authenticated Billit user. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from Billit. |
| [Get Order](actions/get-order.md) | GET | Retrieves a Billit order by ID. |
| [List Orders](actions/list-orders.md) | GET | Retrieves Billit orders for the authenticated company. |
| [Update Order Export Status](actions/update-order-export-status.md) | PUT | Updates a Billit order's export status and internal note. |

### Party

| Action | Method | Description |
| --- | --- | --- |
| [Create Party](actions/create-party.md) | POST | Creates a new party in Billit. |
| [Get Party](actions/get-party.md) | GET | Retrieves a Billit party by ID. |
| [List Parties](actions/list-parties.md) | GET | Retrieves Billit parties for the authenticated company. |
| [Update Party](actions/update-party.md) | PUT | Updates an existing party in Billit. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a Billit product by ID. |
| [List Products](actions/list-products.md) | GET | Retrieves Billit products for the authenticated company. |

### Sales Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Invoice](actions/create-sales-invoice.md) | POST | Creates a sales invoice in Billit. |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Get Next Invoice Sequence](actions/get-next-invoice-sequence.md) | GET | Retrieves the next Billit invoice sequence preview. |

