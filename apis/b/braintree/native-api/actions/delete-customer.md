# Delete Customer with Braintree

Deletes an existing customer from Braintree.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://payments.sandbox.braintree-api.com`
- **Official documentation:** [Delete Customer](https://developer.paypal.com/braintree/graphql/reference/#Mutation--deleteCustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.customerId` | body | `string` | yes | The GraphQL ID of the customer to delete. |
