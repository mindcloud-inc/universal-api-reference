# Get Customer Net Balance with Metronome

Retrieves a customer's net balance from Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contracts/customerBalances/getNetBalance`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Get Customer Net Balance](https://docs.metronome.com/api-reference/credits-and-commits/get-the-net-balance-of-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | The customer ID. |
