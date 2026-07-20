# Get Page with Content Snare

Retrieves a page from Content Snare.

## Endpoint

- **Method:** `GET`
- **Path:** `/partner_api/v1/pages/{id}`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Get Page](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Page ID. |
| `include_internal_fields` | query | `boolean` | no | Specifies whether to include fields marked as internal in the response |
