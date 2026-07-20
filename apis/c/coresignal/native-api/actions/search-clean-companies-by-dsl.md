# Search Clean Companies By DSL with Coresignal

Finds clean companies in Coresignal with an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/company_clean/search/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Search Clean Companies By DSL](https://docs.coresignal.com/api/clean-company-api-esdsl-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Elasticsearch DSL query object. |
