# Search People with People Data Labs

## Endpoint

- **Method:** `GET`
- **Path:** `/person/search`
- **Base URL:** `https://api.peopledatalabs.com/v5`
- **Official documentation:** [Search People](https://docs.peopledatalabs.com/docs/reference-person-search-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sql` | query | `string` | yes | SQL query used to search People Data Labs person records. Must be of the form SELECT * FROM person WHERE ... |
