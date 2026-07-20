# Capture Transaction with Payrexx

Captures a transaction in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Transaction/:id/capture`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Capture Transaction](https://developers.payrexx.com/reference/capture-a-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the transaction to capture. |
