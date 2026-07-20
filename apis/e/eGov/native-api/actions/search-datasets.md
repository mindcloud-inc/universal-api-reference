# Search Datasets with e-Gov

Finds datasets in e-Gov by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/package_search`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Search Datasets](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Solr query string. Leave blank to search all datasets. |
| `fq` | query | `string` | no | — |
| `sort` | query | `string` | no | — |
| `rows` | query | `number` | no | Maximum number of datasets to return. |
| `start` | query | `number` | no | Result offset. |
| `facet` | query | `boolean` | no | — |
| `facet.mincount` | query | `number` | no | — |
| `facet.limit` | query | `number` | no | — |
