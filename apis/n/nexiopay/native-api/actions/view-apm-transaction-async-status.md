# View APM transaction async status with Nexiopay

## Endpoint

- **Method:** `GET`
- **Path:** `/apm/v3/transactionAsyncStatus/{asyncTraceId}`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [View APM transaction async status](https://docs.nexiopay.com/reference/viewapmtransactionasyncstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asyncTraceId` | path | `string` | yes | APM async trace ID returned by the transaction request. |
