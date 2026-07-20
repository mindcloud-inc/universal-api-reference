# Capture an APM transaction with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/apm/v3/capture`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Capture an APM transaction](https://docs.nexiopay.com/reference/captureapmtransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Nexio APM payment ID to capture. |
| `data` | body | `object` | yes | APM capture data object documented by Nexio. |
