# Get Customer with Priority

Retrieves a customer from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/CUSTOMERS(CUSTNAME=':custName')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Customer](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CUSTNAME` | path | `string` | yes | Priority customer key. |
