# Add Customer with ReputationLync

Creates a new customer in ReputationLync.

## Endpoint

- **Method:** `POST`
- **Path:** `/addCustomer`
- **Base URL:** `https://reputationlync.com/app/api/customer`
- **Official documentation:** [Add Customer](https://documenter.getpostman.com/view/25361963/2s93Xzw2bS#46718236-5ef1-4c93-992d-cd7d3722b02f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_name` | body | `string` | yes | Name of the customer to add. |
| `email_id` | body | `string` | no | Customer email address. Provide this or Phone Number. |
| `phone_number` | body | `string` | no | Customer phone number. Provide this or Email ID. |
| `whatsapp_enabled` | body | `string` | no | Use 1 if the phone number is WhatsApp-enabled, otherwise 0. |
| `tags` | body | `string` | no | Comma-separated tags to associate with the customer. |
| `language` | body | `string` | no | Language configured in ReputationLync for this customer. |
| `source` | body | `string` | no | Source label for this customer creation. |
| `source_xref_id` | body | `string` | no | External customer or transaction ID from the source system. |
