# Register terminal with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/pay/v3/registerTerminal`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Register terminal](https://docs.nexiopay.com/reference/registerterminal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `merchantId` | body | `string` | yes | Nexio merchant ID to associate with the terminal. |
| `terminalRegistrationCode` | body | `string` | yes | Registration code shown by the terminal. |
