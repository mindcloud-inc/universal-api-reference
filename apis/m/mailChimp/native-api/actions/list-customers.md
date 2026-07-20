# List Customers with Mailchimp

Retrieves customers from a Mailchimp e-commerce store.

## Endpoint

- **Method:** `GET`
- **Path:** `ecommerce/stores/:store_id/customers`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [List Customers](https://mailchimp.com/developer/marketing/api/ecommerce-customers/list-customers/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | query | `string` | no | — |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `store_id` | path | `string` | yes | The store id. |
