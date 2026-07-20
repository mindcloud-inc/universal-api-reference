# List Customer Balances with Metronome

Retrieves balances for a customer from Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contracts/customerBalances/list`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [List Customer Balances](https://docs.metronome.com/api-reference/credits-and-commits/list-balances)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | The customer ID. |
