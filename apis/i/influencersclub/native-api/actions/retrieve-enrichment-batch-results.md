# Retrieve Enrichment Batch Results with Influencers.club

Retrieves batch enrichment results from Influencers.club.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v1/enrichment/batch/:batch_id/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Retrieve Enrichment Batch Results](https://docs.influencers.club/openapi/batch-enrichment/public_v1_enrichment_batch_retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | yes | Batch identifier from create enrichment batch response. |
