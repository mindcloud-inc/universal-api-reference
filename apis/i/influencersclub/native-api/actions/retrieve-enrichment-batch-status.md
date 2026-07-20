# Retrieve Enrichment Batch Status with Influencers.club

Retrieves batch enrichment job status from Influencers.club.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v1/enrichment/batch/:batch_id/status/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Retrieve Enrichment Batch Status](https://docs.influencers.club/openapi/batch-enrichment/public_v1_enrichment_batch_status_retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | yes | Batch identifier to check status. |
