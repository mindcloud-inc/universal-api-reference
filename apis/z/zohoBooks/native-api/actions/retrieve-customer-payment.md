# Retrieve Customer Payment with Zoho Books

## Endpoint

- **Method:** `GET`
- **Path:** `/customerpayments/:payment_id`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Retrieve Customer Payment](https://www.zoho.com/books/api/v3/customer-payments/#retrieve-a-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accept` | query | `string` | no | Response format: json or pdf. |
| `organization_id` | query | `string` | yes | ID of the organization. |
| `payment_id` | path | `string` | yes | Unique identifier of the payment. |
