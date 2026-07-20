# Delete Filter with TrueMail

Deletes an existing blocklist filter from TrueMail.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/filters/{{id}}`
- **Base URL:** `https://api.mailcop.net`
- **Official documentation:** [Delete Filter](https://mailcop.net/docs/api-filters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The filter identifier to delete. |
