# Search Transactions with Braintree

Finds transactions in Braintree by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://payments.sandbox.braintree-api.com`
- **Official documentation:** [Search Transactions](https://developer.paypal.com/braintree/graphql/reference/#Query--search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.id.is` | body | `string` | no | Exact GraphQL transaction ID to search for. This filter does not accept the legacy transaction ID. |
| `variables.input.status.is` | body | `string` | no | Exact transaction status to search for. |
