# Capture a transaction with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/capture`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Capture a transaction](https://docs.nexiopay.com/reference/capturetransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Nexio payment ID to capture. |
| `data` | body | `object` | yes | Capture transaction data object documented by Nexio. |
