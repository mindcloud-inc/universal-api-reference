# Get Part Balance with Priority

Retrieves a part balance from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/PARTBAL(WARHS=:warhs,PART=:part,CUST=:cust,ACT=:act,SERIAL=:serial)`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Part Balance](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `WARHS` | path | `number` | yes | Priority warehouse key for the part balance lookup. |
| `PART` | path | `number` | yes | Priority part key for the part balance lookup. |
| `CUST` | path | `number` | yes | Priority customer segment of the composite part balance key. |
| `ACT` | path | `number` | yes | Priority activity segment of the composite part balance key. |
| `SERIAL` | path | `number` | yes | Priority serial segment of the composite part balance key. |
