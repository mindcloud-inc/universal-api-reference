# Create Segment with Leadboxer

Creates a new segment in Leadboxer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/segments`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Create Segment](https://developers.leadboxer.com/reference/createsegment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The user email address. |
| `name` | body | `string` | yes | Segment name. |
| `accountId` | body | `string` | yes | The Leadboxer account ID. |
| `datasetId` | body | `string` | yes | The dataset ID. |
| `type` | body | `string` | yes | Segment visibility type. |
