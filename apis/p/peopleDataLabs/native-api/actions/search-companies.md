# Search Companies with People Data Labs

## Endpoint

- **Method:** `GET`
- **Path:** `/company/search`
- **Base URL:** `https://api.peopledatalabs.com/v5`
- **Official documentation:** [Search Companies](https://docs.peopledatalabs.com/docs/reference-company-search-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sql` | query | `string` | yes | People Data Labs company search SQL clause in the form SELECT * FROM company WHERE ... |
