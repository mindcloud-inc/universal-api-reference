# List Stage0 Entries with Inistate

Retrieves Stage0 entries from Inistate.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/workspace/list`
- **Base URL:** `https://api.inistate.com`
- **Official documentation:** [List Stage0 Entries](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currentPage` | body | `number` | no | Zero-based page number. |
| `pageSize` | body | `number` | no | Number of entries to return per page. Use 0 only if you intentionally want the provider's all-rows behavior. |
| `filters` | body | `object` | no | Optional QueryFilterProcessor payload. Use the provider's documented `filters.items` structure; sorting is intentionally omitted because live provider runs currently fail when `sorts` is supplied. |
