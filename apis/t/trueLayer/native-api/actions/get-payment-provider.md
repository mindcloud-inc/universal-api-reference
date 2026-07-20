# Get Payment Provider with TrueLayer

Retrieves a payment provider from TrueLayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/payments-providers/:id`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Get Payment Provider](https://docs.truelayer.com/reference/get-payment-provider)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment provider ID, such as mock-payments-gb-redirect. |
