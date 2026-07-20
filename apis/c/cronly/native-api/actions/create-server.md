# Create Server with Cronly

## Endpoint

- **Method:** `POST`
- **Path:** `/api/servers`
- **Base URL:** `https://cronly.app`
- **Official documentation:** [Create Server](https://docs.cronly.app/api/servers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the server. |
| `ip_address` | body | `string` | yes | The IP address of the server. |
| `identifier` | body | `string` | yes | The server identifier. |
