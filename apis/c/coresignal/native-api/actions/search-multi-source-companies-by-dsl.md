# Search Multi-source Companies By DSL with Coresignal

Finds multi-source companies in Coresignal with an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/company_multi_source/search/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Search Multi-source Companies By DSL](https://docs.coresignal.com/company-api/multi-source-company-api/elasticsearch-dsl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Elasticsearch DSL query object. |
