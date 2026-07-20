# Search Core Autocomplete with Next Cloud OCS

Finds core autocomplete in Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v2.php/core/autocomplete/get`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Search Core Autocomplete](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#auto-complete-and-user-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | — |
| `search` | query | `string` | yes | — |
| `shareTypes[]` | query | `string` | no | Send multiple values as a array. |
