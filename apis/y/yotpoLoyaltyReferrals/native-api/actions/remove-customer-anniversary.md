# Remove Customer Anniversary with Yotpo Loyalty & Referrals

Deletes a customer's anniversary from Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/customer_anniversary`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Remove Customer Anniversary](https://loyaltyapi.yotpo.com/reference/remove-customer-anniversary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_email` | body | `string` | yes | The customer's email address. |
