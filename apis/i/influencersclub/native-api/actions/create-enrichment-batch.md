# Create Enrichment Batch with Influencers.club

Creates a batch enrichment job in Influencers.club from a CSV.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/enrichment/batch/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Create Enrichment Batch](https://docs.influencers.club/openapi/batch-enrichment/public_v1_enrichment_batch_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | CSV file (single column handle or email). |
| `enrichment_mode` | body | `string` | yes | Mode: raw, full, basic, or advanced. |
| `platform` | body | `string` | no | Platform for handle-based enrichment batches. |
