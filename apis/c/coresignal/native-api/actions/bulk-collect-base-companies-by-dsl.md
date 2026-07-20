# Bulk Collect Base Companies By DSL with Coresignal

Creates a bulk base company DSL collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/company_base/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Base Companies By DSL](https://docs.coresignal.com/company-api/base-company-api/endpoints/bulk-collect-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `es_dsl_query` | body | `object` | yes | Elasticsearch DSL query object for Base Company bulk collect. |
