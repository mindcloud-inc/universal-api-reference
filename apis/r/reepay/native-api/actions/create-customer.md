# Create Customer with Reepay

Creates a new customer in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customer`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Create Customer](https://docs.frisbii.com/reference/createcustomerjson)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | body | `string` | no |
| `address2` | body | `string` | no |
| `city` | body | `string` | no |
| `company` | body | `string` | no |
| `country` | body | `string` | no |
| `debtor_id` | body | `number` | no |
| `dunning_email` | body | `string` | no |
| `email` | body | `string` | no |
| `first_name` | body | `string` | no |
| `generate_handle` | body | `boolean` | no |
| `handle` | body | `string` | no |
| `invoice_email` | body | `string` | no |
| `language` | body | `string` | no |
| `last_name` | body | `string` | no |
| `metadata` | body | `object` | no |
| `phone` | body | `string` | no |
| `postal_code` | body | `string` | no |
| `test` | body | `boolean` | no |
| `vat` | body | `string` | no |
