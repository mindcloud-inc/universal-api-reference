# Search Suppliers with Zahara

Finds suppliers in Zahara by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/{businessUnitApiKey}/Supplier/Search/{{searchTerm}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Search Suppliers](https://ask.zaharasoftware.com/api-docs/get-suppliers-by-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchTerm` | path | `string` | yes | Supplier search text. |
