# Get Subscription Proration Details with Pinghome

Retrieves subscription proration details from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment-query/v1/subscription/:id/proration/:product_id`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Get Subscription Proration Details](https://docs.pinghome.io/billing-operations-management/get-subscription-proration-details/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | The subscription ID. |
| `product_id` | path | `string` | no | The product ID to compare for proration. |
