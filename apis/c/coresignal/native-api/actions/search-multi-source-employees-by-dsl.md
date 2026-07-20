# Search Multi-source Employees By DSL with Coresignal

Finds multi-source employees in Coresignal with an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/employee_multi_source/search/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Search Multi-source Employees By DSL](https://docs.coresignal.com/employee-api/multi-source-employee-api/elasticsearch-dsl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Elasticsearch DSL query object. |
