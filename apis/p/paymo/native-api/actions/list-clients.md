# List Clients with Paymo

Retrieves clients from Paymo.

## Endpoint

- **Method:** `GET`
- **Path:** `clients`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [List Clients](https://github.com/paymo-org/api/blob/master/sections/clients.md#getting-clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `where` | query | `string` | no | Optional Paymo filtering expression, for example `name like Sample` or `id>0`. |
