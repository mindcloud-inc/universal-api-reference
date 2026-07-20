# Braintree: Native API Reference

A consolidated summary of Braintree's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://developer.paypal.com/braintree/graphql/reference/
- **API base URL:** `https://payments.sandbox.braintree-api.com`

## Authentication

### API Keys

Use the Braintree GraphQL Basic authorization token. Build the token by base64-encoding `public_key:private_key`, then store that base64 value as the test connection credential.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.paypal.com/braintree/graphql/guides/making_api_calls/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client Token](actions/create-client-token.md) | `POST /graphql` | [docs](https://developer.paypal.com/braintree/graphql/reference/#Mutation--createClientToken) |
| [Create Customer](actions/create-customer.md) | `POST /graphql` | [docs](https://developer.paypal.com/braintree/graphql/reference/#Mutation--createCustomer) |
| [Delete Customer](actions/delete-customer.md) | `POST /graphql` | [docs](https://developer.paypal.com/braintree/graphql/reference/#Mutation--deleteCustomer) |
| [Find Transaction](actions/find-transaction.md) | `POST /graphql` | [docs](https://developer.paypal.com/braintree/graphql/reference/#Query--node) |
| [Ping](actions/ping.md) | `POST /graphql` | [docs](https://developer.paypal.com/braintree/graphql/reference/#Query--ping) |
| [Search Customers](actions/search-customers.md) | `POST /graphql` | [docs](https://developer.paypal.com/braintree/graphql/reference/#Query--search) |
| [Search Transactions](actions/search-transactions.md) | `POST /graphql` | [docs](https://developer.paypal.com/braintree/graphql/reference/#Query--search) |
| [Update Customer](actions/update-customer.md) | `POST /graphql` | [docs](https://developer.paypal.com/braintree/graphql/reference/#Mutation--updateCustomer) |
