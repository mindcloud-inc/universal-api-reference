# Top up subscription wallet with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/payment/stripe/topup`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Top up subscription wallet](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quantity` | body | `number` | no | The quantity of credits to top up |
