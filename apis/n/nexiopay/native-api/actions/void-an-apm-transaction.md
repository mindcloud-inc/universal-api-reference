# Void an APM transaction with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/apm/v3/void`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Void an APM transaction](https://docs.nexiopay.com/reference/voidapmtransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Nexio APM payment ID to void. |
