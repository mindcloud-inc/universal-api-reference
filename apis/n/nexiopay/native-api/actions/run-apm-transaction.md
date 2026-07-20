# Run APM transaction with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/apm/v3/process`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Run APM transaction](https://docs.nexiopay.com/reference/runapmtransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apm` | body | `object` | yes | Alternative payment method token object documented by Nexio. |
| `data` | body | `object` | yes | APM transaction data object documented by Nexio. |
