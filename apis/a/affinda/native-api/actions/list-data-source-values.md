# List values for a data source with Affinda

Retrieves values from an Affinda mapping data source.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/mapping_data_sources/:identifier/values`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [List values for a data source](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotation` | query | `string` | no | Filter based on annotation ID |
| `document` | query | `string` | no | Identifier of the document to apply filter lookups on if available |
| `identifier` | path | `string` | yes | Data source's identifier |
| `limit` | query | `string` | no | The numbers of results to return. |
| `offset` | query | `string` | no | The number of documents to skip before starting to collect the result set. |
| `search` | query | `string` | no | Search for specific values |
