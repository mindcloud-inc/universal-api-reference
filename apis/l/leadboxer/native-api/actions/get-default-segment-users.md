# Get Default Segment Users with Leadboxer

Retrieves user IDs for a default segment in Leadboxer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/segment/preference`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Get Default Segment Users](https://developers.leadboxer.com/reference/getusersbysegmentidanddatasetid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `segmentId` | query | `number` | yes |
| `datasetId` | query | `string` | yes |
