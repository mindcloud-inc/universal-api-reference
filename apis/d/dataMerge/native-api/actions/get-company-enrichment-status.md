# Get Company Enrichment Status with DataMerge

Retrieves a DataMerge company enrichment job status.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/company/enrich/:job_id/status`
- **Base URL:** `https://api.datamerge.ai`
- **Official documentation:** [Get Company Enrichment Status](https://api.datamerge.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Company enrichment job ID. |
