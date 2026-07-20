# Create Contract with Metronome

Creates a new contract in Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contracts/create`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Create Contract](https://docs.metronome.com/api-reference/contracts/create-a-contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | The customer ID. |
| `starting_at` | body | `string` | yes | Inclusive contract start time. |
