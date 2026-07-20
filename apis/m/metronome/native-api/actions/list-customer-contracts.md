# List Customer Contracts with Metronome

Retrieves contracts for a customer from Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/contracts/list`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [List Customer Contracts](https://docs.metronome.com/api-reference/contracts/list-customer-contracts-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | The customer ID. |
