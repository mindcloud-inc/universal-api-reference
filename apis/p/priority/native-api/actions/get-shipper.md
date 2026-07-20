# Get Shipper with Priority

Retrieves a shipper from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/SHIPPERS(SHIPPERNAME=':shipperName')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Shipper](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SHIPPERNAME` | path | `string` | yes | Priority shipper key. |
