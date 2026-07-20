# Set Customer Birthday with Yotpo Loyalty & Referrals

Updates a customer's birthday in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customer_birthdays`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Set Customer Birthday](https://loyaltyapi.yotpo.com/reference/set-customer-birthday)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_email` | body | `string` | no | The customer's email address. Provide this or Customer ID. |
| `customer_id` | body | `string` | no | The identifier used to uniquely identify the customer in your system. Provide this or Customer Email. |
| `day` | body | `number` | yes | The day of the month for the customer's birthday. |
| `month` | body | `number` | yes | The month of the year for the customer's birthday. |
| `year` | body | `number` | no | The optional year for the customer's birthday. |
