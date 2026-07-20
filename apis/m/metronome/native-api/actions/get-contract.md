# Get Contract with Metronome

Retrieves a contract from Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/contracts/get`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Get Contract](https://docs.metronome.com/api-reference/contracts/get-a-contract-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | The customer ID. |
| `contract_id` | body | `string` | yes | The contract ID. |
