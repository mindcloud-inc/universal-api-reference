# Create Customer with Braintree

Creates a new customer in Braintree.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://payments.sandbox.braintree-api.com`
- **Official documentation:** [Create Customer](https://developer.paypal.com/braintree/graphql/reference/#Mutation--createCustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.customer.firstName` | body | `string` | no | Customer first name. |
| `variables.input.customer.lastName` | body | `string` | no | Customer last name. |
| `variables.input.customer.email` | body | `string` | no | Customer email address. |
| `variables.input.customer.company` | body | `string` | no | Customer company name. |
