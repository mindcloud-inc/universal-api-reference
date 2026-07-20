# Search Companies with Tomba

Finds companies in Tomba by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/reveal/search`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [Search Companies](https://docs.tomba.io/api/reveal#search-companies)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | body | `string` | no |
| `filters` | body | `object` | no |
| `page` | body | `number` | no |
