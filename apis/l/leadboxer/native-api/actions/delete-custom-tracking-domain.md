# Delete Custom Tracking Domain with Leadboxer

Deletes a custom tracking domain from a dataset in Leadboxer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/management/ctd/{{datasetId}}`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Delete Custom Tracking Domain](https://developers.leadboxer.com/reference/deletecustomtrackingdomain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ctd` | query | `string` | yes | The custom tracking domain to delete. |
| `datasetId` | path | `string` | yes | The dataset ID. |
