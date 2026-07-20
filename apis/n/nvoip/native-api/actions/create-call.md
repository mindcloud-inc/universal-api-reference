# Create Call with Nvoip

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/`
- **Base URL:** `https://api.nvoip.com.br/v2`
- **Official documentation:** [Create Call](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/calls.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `called` | body | `string` | yes | Destino da chamada. |
| `caller` | body | `string` | yes | Origem da chamada. |
