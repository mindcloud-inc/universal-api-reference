# Search Multi-source Jobs By DSL with Coresignal

Finds multi-source jobs in Coresignal with an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/job_multi_source/search/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Search Multi-source Jobs By DSL](https://docs.coresignal.com/jobs-api/multi-source-jobs-api/elasticsearch-dsl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Elasticsearch DSL query object. |
