# Create Customer with Razorpay

Creates a new customer in Razorpay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Create Customer](https://razorpay.com/docs/api/customers/create/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `contact` | body | `string` | no |
| `email` | body | `string` | no |
| `fail_existing` | body | `string` | no |
| `gstin` | body | `string` | no |
| `notes` | body | `object` | no |
