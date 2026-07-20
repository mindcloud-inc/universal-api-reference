# Bulk Collect Multi-source Companies By DSL with Coresignal

Creates a bulk multi-source company DSL collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/company_multi_source/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Multi-source Companies By DSL](https://docs.coresignal.com/company-api/multi-source-company-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `es_dsl_query` | body | `object` | yes |
