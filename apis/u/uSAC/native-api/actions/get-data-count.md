# Get Data Count with USAC

## Endpoint

- **Method:** `GET`
- **Path:** `resource/:resourceId.json`
- **Base URL:** `https://opendata.usac.org/api/`
- **Official documentation:** [Get Data Count](https://dev.socrata.com/docs/queries/select)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | This is the ID of the dataset, use the List Datasets action to retrieve this. |
| `$select` | query | `string` | yes | Used similar to SQL where. Docs: https://dev.socrata.com/docs/queries/select |
