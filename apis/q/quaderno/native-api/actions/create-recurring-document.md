# Create Recurring Document with Quaderno

Creates a recurring billing document in Quaderno.

## Endpoint

- **Method:** `POST`
- **Path:** `/recurring`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Create Recurring Document](https://developers.quaderno.io/api/#tag/Recurring-Documents/operation/createRecurring)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | body | `date` | no | Issue date for the first recurring document. |
| `end_date` | body | `date` | no | Issue date for the last recurring document. |
| `frequency` | body | `string` | no | Deprecated recurring frequency option. |
| `recurring_period` | body | `string` | no | Recurring period unit. |
| `recurring_frequency` | body | `number` | no | Number of recurring periods between documents. |
| `due_days` | body | `string` | no | Number of days until payment is due. |
| `currency` | body | `string` | no | Three-letter ISO currency code. |
| `payment_details` | body | `string` | no | Accepted payment method details. |
| `notes` | body | `string` | no | Extra notes for the recurring document. |
| `contact.first_name` | body | `string` | yes | Contact first name. |
| `contact.last_name` | body | `string` | no | Contact last name. |
| `contact.email` | body | `string` | no | Contact email address. |
| `contact.country` | body | `string` | no | Two-letter ISO country code for the contact. |
| `subject` | body | `string` | no | Summary description for the recurring document. |
| `items[].description` | body | `string` | yes | Line item description. |
| `items[].quantity` | body | `number` | no | Line item quantity. |
| `items[].unit_price` | body | `number` | yes | Line item unit price. |
| `items[].tax_1_transaction_type` | body | `string` | no | Primary tax classification for the line item. |
| `custom_metadata` | body | `object` | no | Custom metadata object for the recurring document. |
