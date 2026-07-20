# Get Currency with Priority

Retrieves a currency from Priority.

## Endpoint

- **Method:** `GET`
- **Path:** `/CURRENCIES(CODE=':code')`
- **Base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`
- **Official documentation:** [Get Currency](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CODE` | path | `string` | yes | Priority currency code key. |
