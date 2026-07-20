# Get Build Status With Elements with Graphor

Retrieves source build status and elements from Graphor.

## Endpoint

- **Method:** `GET`
- **Path:** `/builds/{buildId}`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Get Build Status With Elements](https://docs.graphorlm.com/api-reference/sources/upload#get-build-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build_id` | path | `string` | yes | The build identifier returned by an ingestion or reprocess request. |
