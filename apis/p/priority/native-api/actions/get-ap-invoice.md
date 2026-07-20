# Get AP Invoice with Priority

Retrieves an AP invoice from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/PINVOICES(IVNUM=':ivNum',DEBIT=':debit',IVTYPE=':ivType')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get AP Invoice](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `IVNUM` | path | `string` | yes | Priority invoice number key. |
| `DEBIT` | path | `string` | yes | Priority debit indicator key. |
| `IVTYPE` | path | `string` | yes | Priority invoice type key. |
