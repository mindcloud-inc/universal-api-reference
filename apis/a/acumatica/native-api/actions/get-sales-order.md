# Get Sales Order with Acumatica

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/{endpointName}/{endpointVersion}/SalesOrder/:orderType/:orderNbr`
- **Base URL:** `{uRL}`
- **Official documentation:** [Get Sales Order](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-Key-Fields)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderType` | path | `string` | yes | The Acumatica sales order type returned by List Sales Orders. |
| `orderNbr` | path | `string` | yes | The Acumatica sales order number returned by List Sales Orders. |
| `$select` | query | `string` | no | Fields to return, using Acumatica $select syntax. |
| `$expand` | query | `string` | no | — |
| `$custom` | query | `string` | no | Custom fields to return, using Acumatica $custom syntax. |
