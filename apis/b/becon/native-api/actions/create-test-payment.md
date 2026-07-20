# Create Test Payment with Becon

Creates a test payment in Becon.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/test`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Create Test Payment](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Output address when simulating a BTC store payment. |
| `currency_id` | body | `string` | yes | Currency id to simulate. |
| `memo` | body | `string` | no | Memo when simulating a BNB store payment. |
| `store_id` | body | `string` | yes | Target store id to simulate. |
| `sum` | body | `string` | yes | Payment amount to simulate. |
| `transaction_id` | body | `string` | yes | Test blockchain transaction id string. |
