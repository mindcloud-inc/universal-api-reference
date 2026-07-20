# List transactions with Wisewand

Retrieves transactions from your Wisewand workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transactions/`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [List transactions](https://api.wisewand.ai/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | ISO 8601 format |
| `end_date` | query | `string` | no | ISO 8601 format |
| `reason` | query | `string` | no | Filter by reason(s). Can be a single value or multiple values separated by commas (e.g., "payment,task_run") |
| `debits_only` | query | `boolean` | no | Filter to show only debit transactions (negative credits) |
