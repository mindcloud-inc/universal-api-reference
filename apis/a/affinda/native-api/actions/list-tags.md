# Get list of all tags with Affinda

Retrieves all accessible tags from Affinda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/tags`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Get list of all tags](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | The numbers of results to return. |
| `name` | query | `string` | no | Filter by name. |
| `offset` | query | `string` | no | The number of documents to skip before starting to collect the result set. |
| `workspace` | query | `string` | no | Filter by workspace. |
