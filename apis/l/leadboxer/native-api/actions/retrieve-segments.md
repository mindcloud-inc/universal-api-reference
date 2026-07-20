# Retrieve Segments with Leadboxer

Retrieves segments from Leadboxer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/segments`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Retrieve Segments](https://developers.leadboxer.com/reference/getsegments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The user email address. |
| `accountId` | query | `string` | yes | The Leadboxer account ID. |
| `datasetId` | query | `string` | yes | The dataset ID. |
