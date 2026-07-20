# Delete Token with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/token/delete`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Delete Token](https://docs.paytabs.com/manuals/PT-API-Endpoints/Token-Based-Transactions/Step-3-Managing-Token/Token-Based-Transactions-Delete-Token/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | Stored PayTabs token to revoke. |
