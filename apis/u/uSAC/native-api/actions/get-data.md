# Get Data with USAC

## Endpoint

- **Method:** `GET`
- **Path:** `resource/:resourceId.json`
- **Base URL:** `https://opendata.usac.org/api/`
- **Official documentation:** [Get Data](https://dev.socrata.com/docs/filtering)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | This is the ID of the dataset, use the List Datasets action to retrieve this. |
| `$where` | query | `string` | no | Used similar to SQL where. Docs: https://dev.socrata.com/docs/queries/where |
| `$order` | query | `string` | no | — |
