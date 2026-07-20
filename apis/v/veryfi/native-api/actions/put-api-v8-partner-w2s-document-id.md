# Update a W-2 with Veryfi

Updates an existing W-2 in Veryfi.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v8/partner/w2s/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Update a W-2](https://docs.veryfi.com/api/w2s/update-a-w-2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `external_id` | body | `string` | no | Possible values: non-empty Deprecated 2025-01-09, use meta.external_id instead. |
| `meta` | body | `string` | no | Possible values: non-empty Possible values: non-empty Default value: `` |
