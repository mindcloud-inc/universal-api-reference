# Preview Multi-source Jobs By DSL with Coresignal

Previews multi-source jobs in Coresignal from an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/job_multi_source/search/es_dsl/preview`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Preview Multi-source Jobs By DSL](https://docs.coresignal.com/job-api/multi-source-job-api/endpoints/preview-jobs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | body | `object` | yes |
