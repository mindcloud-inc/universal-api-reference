# Get Build Status with Graphor

Retrieves source build status from Graphor by build ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/builds/{buildId}`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Get Build Status](https://docs.graphorlm.com/api-reference/sources/upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build_id` | path | `string` | yes | The build identifier returned by an ingestion or reprocess request. |
| `page` | query | `string` | no | 1-based page number for paginated build elements. |
| `page_size` | query | `string` | no | Number of build elements to return per page when pagination is used. |
