# Create Payment Gateway Session with Rye

Creates a payment gateway session in Rye.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/payment-gateways/{gateway}/session`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [Create Payment Gateway Session](https://rye.com/docs/api-v2/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gateway` | path | `string` | yes | The payment gateway to create a session for. |
