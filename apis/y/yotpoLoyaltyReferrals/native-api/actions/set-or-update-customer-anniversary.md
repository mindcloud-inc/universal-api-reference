# Set or Update Customer Anniversary with Yotpo Loyalty & Referrals

Updates a customer's anniversary in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customer_anniversary`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Set or Update Customer Anniversary](https://loyaltyapi.yotpo.com/reference/createupdate-customer-anniversary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_email` | body | `string` | yes | The customer's email address. |
| `day` | body | `number` | yes | The day of the month for the anniversary. |
| `month` | body | `number` | yes | The month of the year for the anniversary. |
| `year` | body | `number` | no | The optional year for the anniversary. |
