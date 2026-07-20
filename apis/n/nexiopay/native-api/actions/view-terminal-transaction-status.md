# View terminal transaction status with Nexiopay

## Endpoint

- **Method:** `GET`
- **Path:** `/pay/v3/processFromTerminal/{terminalRequestId}`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [View terminal transaction status](https://docs.nexiopay.com/reference/viewterminaltransactionstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `terminalRequestId` | path | `string` | yes | Terminal request ID returned by a terminal transaction request. |
