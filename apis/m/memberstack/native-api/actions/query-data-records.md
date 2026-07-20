# Query Data Records with Memberstack

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/data-tables/:tableKey/records/query`
- **Base URL:** `https://admin.memberstack.com`
- **Official documentation:** [Query Data Records](https://developers.memberstack.com/admin-rest-api/data-tables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableKey` | path | `string` | yes | Target data table key. |
| `query` | body | `object` | yes | Query payload (filters, sorting, limits, and cursor fields). |
