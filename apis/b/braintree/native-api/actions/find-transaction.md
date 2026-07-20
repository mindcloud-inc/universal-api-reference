# Find Transaction with Braintree

Retrieves a transaction from Braintree by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://payments.sandbox.braintree-api.com`
- **Official documentation:** [Find Transaction](https://developer.paypal.com/braintree/graphql/reference/#Query--node)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The GraphQL ID of the transaction to fetch. |
