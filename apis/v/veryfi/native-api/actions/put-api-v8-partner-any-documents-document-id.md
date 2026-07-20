# Update a âDoc with Veryfi

Updates an existing AnyDoc in Veryfi.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v8/partner/any-documents/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Update a âDoc](https://docs.veryfi.com/api/anydocs/update-a-A-doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `external_id` | body | `string` | no | Possible values: non-empty Deprecated 2025-01-09, use meta.external_id instead. |
| `meta` | body | `string` | no | Possible values: non-empty Possible values: non-empty Default value: `` |
