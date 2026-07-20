# Update a Contract with Veryfi

Updates an existing contract in Veryfi.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v8/partner/contracts/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Update a Contract](https://docs.veryfi.com/api/contracts/update-a-contract/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `external_id` | body | `string` | no | Possible values: non-empty Deprecated 2025-01-09, use meta.external_id instead. |
| `meta` | body | `string` | no | Possible values: non-empty Possible values: non-empty Default value: `` |
