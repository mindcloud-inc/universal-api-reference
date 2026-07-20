# Get Warehouse with Priority

Retrieves a warehouse from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/WAREHOUSES(WARHSNAME=':warhsName',LOCNAME=':locName')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Warehouse](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `WARHSNAME` | path | `string` | yes | Priority warehouse name key. |
| `LOCNAME` | path | `string` | yes | Priority warehouse location key. |
