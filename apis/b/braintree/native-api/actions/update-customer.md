# Update Customer with Braintree

Updates an existing customer in Braintree.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://payments.sandbox.braintree-api.com`
- **Official documentation:** [Update Customer](https://developer.paypal.com/braintree/graphql/reference/#Mutation--updateCustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.customerId` | body | `string` | yes | The GraphQL ID of the customer to update. |
| `variables.input.customer.company` | body | `string` | no | Updated company value for the customer. |
