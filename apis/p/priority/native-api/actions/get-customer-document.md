# Get Customer Document with Priority

Retrieves a customer document from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/DOCUMENTS_C(DOCNO=':docNo',TYPE=':type')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Customer Document](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DOCNO` | path | `string` | yes | Priority document number key. |
| `TYPE` | path | `string` | yes | Priority document type key. |
