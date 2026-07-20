# <img src="https://images.mindcloud.co/apps/icons/braintree_1773845262251.png" alt="Braintree logo" width="28" height="28"> Braintree: Universal API

Run Braintree payment, customer, subscription, and transaction workflows through the official Braintree GraphQL API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/braintree/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.paypal.com/braintree/
- **Vendor API docs:** https://developer.paypal.com/braintree/graphql/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping](actions/ping.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintree/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Client Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Token](actions/create-client-token.md) | POST | Creates a new client token in Braintree. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Braintree. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Braintree. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in Braintree by search criteria. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Braintree. |

### Query

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Retrieves a ping response from Braintree. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Find Transaction](actions/find-transaction.md) | GET | Retrieves a transaction from Braintree by ID. |
| [Search Transactions](actions/search-transactions.md) | GET | Finds transactions in Braintree by search criteria. |

