# Preview Clean Companies By DSL with Coresignal

Previews clean companies in Coresignal from an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/company_clean/search/es_dsl/preview`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Preview Clean Companies By DSL](https://docs.coresignal.com/company-api/clean-company-api/endpoints/preview-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Elasticsearch DSL query object for Clean Company preview. |
