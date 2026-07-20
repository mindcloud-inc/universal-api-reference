# Create a new subscription for a user with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/payment/stripe/subscription/create`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Create a new subscription for a user](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `priceId` | body | `string` | no | The ID of the price for the subscription plan |
