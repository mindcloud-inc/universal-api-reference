# Update Subscription with Cheddar

Updates an existing subscription in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/edit-subscription/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Update Subscription](https://docs.getcheddar.com/#update-a-subscription-only)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `planCode` | body | `string` | no | Pricing plan code to set on the subscription. |
| `method` | body | `string` | no | Payment method: cc or paypal. |
| `couponCode` | body | `string` | no | Promotion coupon code to apply. |
| `changeBillDate` | body | `date` | no | Date or datetime for the next billable invoice. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
