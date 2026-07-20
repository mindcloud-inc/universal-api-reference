# Preview Base Companies By DSL with Coresignal

Previews base companies in Coresignal from an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/company_base/search/es_dsl/preview`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Preview Base Companies By DSL](https://docs.coresignal.com/company-api/base-company-api/endpoints/preview-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Elasticsearch DSL query object for Base Company preview. |
