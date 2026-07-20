# Get Payment with OxaPay Crypto Payment Gateway

Retrieves a payment from OxaPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/:track_id`
- **Base URL:** `https://api.oxapay.com/v1`
- **Official documentation:** [Get Payment](https://docs.oxapay.com/api-reference/payment/payment-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `track_id` | path | `string` | yes | OxaPay payment track id. |
