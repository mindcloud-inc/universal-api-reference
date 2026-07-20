# List All Lead Notes with leadtributor.cloud

Retrieves notes for all leads in leadtributor.cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes`
- **Base URL:** `https://api.leadtributor.cloud`
- **Official documentation:** [List All Lead Notes](https://developer.leadtributor.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `continuation` | query | `string` | no | Continuation token for the next page of notes. |
| `maxResults` | query | `number` | no | Maximum number of notes to return. |
| `modifiedSince` | query | `string` | no | Filter notes by last modification time. |
