# Legacy Get Payment with TrueLayer

Retrieves a legacy payment from TrueLayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/single-immediate-payment-initiation-requests/:id`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Legacy Get Payment](https://docs.truelayer.com/reference/get-providers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer legacy payment initiation request ID. |
