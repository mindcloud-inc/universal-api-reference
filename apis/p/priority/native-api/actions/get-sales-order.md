# Get Sales Order with Priority

Retrieves a sales order from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/ORDERS(ORDNAME=':ordName')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Sales Order](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ORDNAME` | path | `string` | yes | Priority sales order key. |
