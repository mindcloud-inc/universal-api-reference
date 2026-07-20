# Query Transaction by Reference with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/query`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Query Transaction by Reference](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Query-Transaction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tran_ref` | body | `string` | yes | Unique PayTabs transaction reference to query. |
