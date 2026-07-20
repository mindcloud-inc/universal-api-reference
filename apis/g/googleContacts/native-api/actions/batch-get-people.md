# Batch Get People with Google Contacts

Retrieves multiple people from Google Contacts by resource name.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people\:batchGet`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Batch Get People](https://developers.google.com/people/api/rest/v1/people/getBatchGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceNames` | query | `string<string>` | yes | Person resource name (for now, pass one value, e.g. people/c123). |
| `personFields` | query | `string` | yes | — |
| `sources` | query | `string` | no | — |
