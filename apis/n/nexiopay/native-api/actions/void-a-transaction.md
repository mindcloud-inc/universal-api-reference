# Void a transaction with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/void`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Void a transaction](https://docs.nexiopay.com/reference/voidtransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Nexio payment ID to void. |
