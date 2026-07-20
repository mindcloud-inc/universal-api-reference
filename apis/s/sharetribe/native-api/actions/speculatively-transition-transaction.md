# Speculatively Transition Transaction with Sharetribe

Speculatively transitions a transaction in Sharetribe.

## Endpoint

- **Method:** `POST`
- **Path:** `transactions/transition_speculative`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Speculatively Transition Transaction](https://www.sharetribe.com/api-reference/integration.html#speculatively-transition-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the transaction. |
| `transition` | body | `string` | yes | The name of a possible next transition for the current transaction state. |
| `params` | body | `object` | no | Transition parameters object as required by the transaction process definition. |
