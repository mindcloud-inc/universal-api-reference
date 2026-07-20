# Get Bank with Priority

Retrieves a bank from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/BANKS(BANKCODE=':bankCode')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Bank](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BANKCODE` | path | `string` | yes | Priority bank code key. |
