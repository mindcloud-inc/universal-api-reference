# Update Custom Tracking Domain with Leadboxer

Updates a custom tracking domain for a dataset in Leadboxer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/management/ctd/update`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Update Custom Tracking Domain](https://developers.leadboxer.com/reference/updatedcustomtrackingdomain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ctd` | body | `string` | yes | The custom tracking domain value. |
| `datasetId` | body | `string` | yes | The dataset ID. |
| `description` | body | `string` | no | Optional description for the custom tracking domain. |
