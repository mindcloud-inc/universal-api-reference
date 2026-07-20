# View transaction async status with Nexiopay

## Endpoint

- **Method:** `GET`
- **Path:** `/pay/v3/transactionAsyncStatus/{asyncTraceId}`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [View transaction async status](https://docs.nexiopay.com/reference/viewtransactionasyncstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asyncTraceId` | path | `string` | yes | Async trace ID returned by the transaction request. |
