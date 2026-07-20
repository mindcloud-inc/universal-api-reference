# List Payment Subscriptions with Systeme.io

Retrieves payment subscriptions from Systeme.io for a contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/payment/subscriptions`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [List Payment Subscriptions](https://developer.systeme.io/reference/api_paymentsubscriptions_get_collection-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | query | `number` | yes | Contact identifier used to fetch subscriptions. |
