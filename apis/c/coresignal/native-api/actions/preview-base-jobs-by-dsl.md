# Preview Base Jobs By DSL with Coresignal

Previews base jobs in Coresignal from an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/job_base/search/es_dsl/preview`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Preview Base Jobs By DSL](https://docs.coresignal.com/job-api/base-job-api/endpoints/preview-jobs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | body | `object` | yes |
