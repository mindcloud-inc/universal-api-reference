# Deregister terminal with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/deregisterTerminal`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Deregister terminal](https://docs.nexiopay.com/reference/deregisterterminal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `terminalId` | body | `string` | yes | Nexio terminal ID to deregister. |
