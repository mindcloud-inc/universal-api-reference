# Process transaction from terminal with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/processFromTerminal`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Process transaction from terminal](https://docs.nexiopay.com/reference/processtransactionfromterminal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `terminalId` | body | `string` | yes | Terminal ID returned by the terminal list endpoint. |
| `data` | body | `object` | yes | Retail transaction and customer data object documented by Nexio. |
