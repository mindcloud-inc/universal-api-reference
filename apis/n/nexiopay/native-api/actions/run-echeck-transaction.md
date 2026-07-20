# Run echeck transaction with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/processECheck`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Run echeck transaction](https://docs.nexiopay.com/reference/runechecktransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Transaction and customer data object documented by Nexio. |
| `tokenex` | body | `object` | yes | TokenEx payment token object documented by Nexio. |
