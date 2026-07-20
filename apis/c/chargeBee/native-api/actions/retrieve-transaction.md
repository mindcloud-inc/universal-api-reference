# Retrieve Transaction with ChargeBee

Retrieves a transaction from ChargeBee.

## Endpoint

- **Method:** `GET`
- **Path:** `transactions/:transaction_id`
- **Base URL:** `https://{baseUrl}.chargebee.com/api/v2/`
- **Official documentation:** [Retrieve Transaction](https://apidocs.chargebee.com/docs/api/transactions/retrieve-a-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `string` | yes | The Chargebee transaction identifier. |
