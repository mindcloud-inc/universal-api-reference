# Search Customers with Braintree

Finds customers in Braintree by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://payments.sandbox.braintree-api.com`
- **Official documentation:** [Search Customers](https://developer.paypal.com/braintree/graphql/reference/#Query--search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.company.is` | body | `string` | yes | Exact company value to search for. |
