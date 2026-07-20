# Get list of all validation results with Affinda

Retrieves validation results for an Affinda document.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/validation_results`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Get list of all validation results](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | query | `string` | yes | Filter by document. |
| `limit` | query | `string` | no | The numbers of results to return. |
| `offset` | query | `string` | no | The number of documents to skip before starting to collect the result set. |
