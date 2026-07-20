# Create BNB Test Payment with Becon

Creates a BNB test payment in Becon.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/test`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Create BNB Test Payment](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | The destination crypto address for the sandbox payment. |
| `currency_id` | body | `string` | yes | The Becon currency ID for the test payment. |
| `store_id` | body | `string` | yes | The Becon store ID that owns the test payment. |
| `sum` | body | `string` | yes | The crypto amount to send in the sandbox payment. |
| `transaction_id` | body | `string` | yes | The external transaction ID used by the test payment request. |
