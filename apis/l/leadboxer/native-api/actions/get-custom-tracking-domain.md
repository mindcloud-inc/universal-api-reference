# Get Custom Tracking Domain with Leadboxer

Retrieves custom tracking domains for a dataset in Leadboxer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/management/ctd/{{datasetId}}`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Get Custom Tracking Domain](https://developers.leadboxer.com/reference/getcustomtrackingdomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | Dataset identifier for the LeadBoxer site or website whose custom tracking domain you want to inspect. |
