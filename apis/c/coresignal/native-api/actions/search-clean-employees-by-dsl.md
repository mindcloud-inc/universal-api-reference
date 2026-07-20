# Search Clean Employees By DSL with Coresignal

Finds clean employees in Coresignal with an Elasticsearch DSL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/employee_clean/search/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Search Clean Employees By DSL](https://docs.coresignal.com/api/clean-employee-api-esdsl-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Elasticsearch DSL query object. |
