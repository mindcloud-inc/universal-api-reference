# Search Base Jobs By DSL with Coresignal

Finds base jobs in Coresignal with an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/job_base/search/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Search Base Jobs By DSL](https://docs.coresignal.com/jobs-api/base-jobs-api/endpoints/elasticsearch-dsl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Elasticsearch DSL query object. |
