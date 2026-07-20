# Update a W-8BEN-E with Veryfi

Updates an existing W-8BEN-E in Veryfi.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v8/partner/w-8ben-e/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Update a W-8BEN-E](https://docs.veryfi.com/api/w-8ben-e/update-a-w-8-ben-e/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `external_id` | body | `string` | no | Possible values: non-empty Deprecated 2025-01-09, use meta.external_id instead. |
| `meta` | body | `string` | no | Possible values: non-empty Possible values: non-empty Default value: `` |
