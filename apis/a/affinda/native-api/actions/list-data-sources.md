# List data sources with Affinda

Retrieves custom mapping data sources from Affinda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/mapping_data_sources`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [List data sources](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | query | `string` | no | Filter by identifier. |
| `limit` | query | `string` | no | The numbers of results to return. |
| `name` | query | `string` | no | Filter by name. |
| `offset` | query | `string` | no | The number of documents to skip before starting to collect the result set. |
| `organization` | query | `string` | no | Filter by organization. |
| `workspace` | query | `string` | no | Filter by workspace. |
