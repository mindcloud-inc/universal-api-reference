# Get Enrichment Request with Dropcontact

Retrieves contact enrichment results from Dropcontact.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/enrich/all/{{requestId}}`
- **Base URL:** `https://api.dropcontact.com`
- **Official documentation:** [Get Enrichment Request](https://developer.dropcontact.com/#get-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `forceResults` | query | `boolean` | no | Return partial results even if processing is still running. |
| `requestId` | path | `string` | yes | Request ID returned by the enrich POST call. |
