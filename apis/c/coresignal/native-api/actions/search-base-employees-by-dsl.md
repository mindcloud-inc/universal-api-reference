# Search Base Employees By DSL with Coresignal

Finds base employees in Coresignal with an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/employee_base/search/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Search Base Employees By DSL](https://docs.coresignal.com/api/base-employee-api-esdsl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Elasticsearch DSL query object. |
