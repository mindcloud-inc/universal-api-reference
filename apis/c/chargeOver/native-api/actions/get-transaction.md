# Get Transaction with ChargeOver

Retrieves detailed transaction records from ChargeOver.

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction/:transaction_id`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Get Transaction](https://developer.chargeover.com/docs/api/get-a-specific-transaction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The ChargeOver transaction ID. |
