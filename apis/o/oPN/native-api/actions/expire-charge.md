# Expire Charge with OPN

Expires an existing charge in OPN.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges/:id/expire`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Expire Charge](https://docs.omise.co/charge-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The charge ID to expire. |
