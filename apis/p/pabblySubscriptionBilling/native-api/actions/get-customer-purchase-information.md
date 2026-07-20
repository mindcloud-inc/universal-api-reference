# Get Customer Purchase Information with Pabbly Subscription Billing

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customer/purchase-info/:customerId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [Get Customer Purchase Information](https://apidocs.pabbly.com/#7eceef52-adfc-48a1-9a3f-8c1971f5e024)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency_code` | query | `string` | no | Eg: USD, INR |
| `customer_id` | path | `string` | no | Pabbly Customer ID. |
