# Resume Enrichment Batch with Influencers.club

Resumes a paused batch enrichment job in Influencers.club.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/enrichment/batch/:batch_id/resume/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Resume Enrichment Batch](https://docs.influencers.club/openapi/batch-enrichment/public_v1_enrichment_batch_resume_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | yes | Batch identifier to resume processing. |
