# Edit Contract with Metronome

Updates an existing contract in Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/contracts/edit`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Edit Contract](https://docs.metronome.com/api-reference/contracts/edit-a-contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | The customer ID. |
| `contract_id` | body | `string` | yes | The contract ID. |
| `update_contract_name` | body | `string` | no | Optional new contract name. |
