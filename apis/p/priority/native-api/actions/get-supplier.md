# Get Supplier with Priority

Retrieves a supplier from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/SUPPLIERS(SUPNAME=':supName')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Supplier](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SUPNAME` | path | `string` | yes | Priority supplier key. |
