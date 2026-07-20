# Capture Charge with OPN

Captures an existing charge in OPN.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges/:id/capture`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Capture Charge](https://docs.omise.co/charge-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capture_amount` | body | `number` | no | A partial amount to capture. |
| `id` | path | `string` | yes | The charge ID to capture. |
