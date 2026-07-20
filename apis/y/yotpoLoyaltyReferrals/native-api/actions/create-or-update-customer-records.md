# Create or Update Customer Records with Yotpo Loyalty & Referrals

Creates or updates customer records in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customers`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Create or Update Customer Records](https://loyaltyapi.yotpo.com/reference/createupdate-customer-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The customer's email address. |
| `id` | body | `string` | no | The identifier used to uniquely identify the customer in your system. |
| `first_name` | body | `string` | no | The customer's first name. |
| `last_name` | body | `string` | no | The customer's last name. |
| `phone_number` | body | `string` | no | The customer's phone number in E.164 format. |
| `country_iso_code` | body | `string` | no | Use only if phone number cannot be sent in full E.164 format. |
| `has_account` | body | `boolean` | no | Whether the customer has an account with the eCommerce platform. |
| `opted_in` | body | `boolean` | no | Whether the customer should be opted in to the loyalty program. |
| `platform_account_created_at` | body | `string` | no | Date and time when the customer created an account with your store. |
| `pos_account_id` | body | `string` | no | The point-of-sale unique account identifier. |
| `tags` | body | `string` | no | A comma-separated list of tags or collections this customer belongs to. This overwrites existing tags. |
| `opted_in_at` | body | `string` | no | Date and time when the customer was opted in to the loyalty program. |
