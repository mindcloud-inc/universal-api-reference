# Bulk Collect Multi-source Jobs By DSL with Coresignal

Creates a bulk multi-source job DSL collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/job_multi_source/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Multi-source Jobs By DSL](https://docs.coresignal.com/jobs-api/multi-source-jobs-api/bulk-collect)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `es_dsl_query` | body | `object` | yes |
