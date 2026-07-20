# Remove Default Segment with Leadboxer

Deletes a user's default segment in Leadboxer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/segment/preference`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Remove Default Segment](https://developers.leadboxer.com/reference/deletedefaultsegment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `datasetId` | query | `string` | yes |
