# Enrich Creator By Handle (Full) with Influencers.club

Retrieves full creator enrichment data from Influencers.club by handle.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/creators/enrich/handle/full/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Enrich Creator By Handle (Full)](https://docs.influencers.club/openapi/enrich-by-handle-full/public_v1_creators_enrich_handle_full_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform` | body | `string` | yes | Creator platform (for example instagram). |
| `handle` | body | `string` | yes | Creator handle without @. |
