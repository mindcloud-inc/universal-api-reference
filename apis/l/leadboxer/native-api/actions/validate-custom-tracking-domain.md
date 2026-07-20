# Validate Custom Tracking Domain with Leadboxer

Validates a custom tracking domain in Leadboxer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/management/ctd/validate`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Validate Custom Tracking Domain](https://developers.leadboxer.com/reference/validatecustomtrackingdomain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ctd` | body | `string` | yes | The custom tracking domain value to validate. |
| `datasetId` | body | `string` | yes | The dataset ID. |
| `description` | body | `string` | no | Optional description for the custom tracking domain. |
