# Fetch Customer Details with Yotpo Loyalty & Referrals

Retrieves customer details from Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/customers`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Fetch Customer Details](https://loyaltyapi.yotpo.com/reference/fetch-customer-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_email` | query | `string` | no | The customer's email address. Required if no pos_account_id, customer_id, or phone_number is passed. |
| `customer_id` | query | `string` | no | The identifier used to uniquely identify the customer in your system. Required if no customer_email, pos_account_id, or phone_number is passed. |
| `pos_account_id` | query | `string` | no | The identifier used to uniquely identify the customer in your POS system. Required if no customer_email, customer_id, or phone_number is passed. |
| `phone_number` | query | `string` | no | The customer's phone number in E.164 format. Required if no customer_email, pos_account_id, or customer_id is passed. |
| `country_iso_code` | query | `string` | no | Only use if phone_number cannot be sent in full E.164 format. |
| `with_referral_code` | query | `boolean` | no | Return referral code information when set to true. |
| `with_history` | query | `boolean` | no | Return point earning and redemption history when set to true. |
