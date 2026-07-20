# Enrich Creator By Handle (Raw) with Influencers.club

Retrieves raw creator profile data from Influencers.club by handle.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/creators/enrich/handle/raw/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Enrich Creator By Handle (Raw)](https://docs.influencers.club/openapi/enrich-by-handle-raw/public_v1_creators_enrich_handle_raw_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform` | body | `string` | yes | Creator platform (for example instagram). |
| `handle` | body | `string` | yes | Creator handle without @. |
