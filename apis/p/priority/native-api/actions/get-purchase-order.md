# Get Purchase Order with Priority

Retrieves a purchase order from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/PORDERS(ORDNAME=':ordName')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Purchase Order](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ORDNAME` | path | `string` | yes | Priority purchase order key. |
