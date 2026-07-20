# Add Custom Tracking Domain with Leadboxer

Creates a custom tracking domain in Leadboxer and starts certificate generation.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/management/ctd/add`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Add Custom Tracking Domain](https://developers.leadboxer.com/reference/addcustomtrackingdomain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ctd` | body | `string` | yes | The custom tracking domain to add. |
| `datasetId` | body | `string` | yes | The dataset ID. |
| `description` | body | `string` | no | Optional description for the custom tracking domain. |
