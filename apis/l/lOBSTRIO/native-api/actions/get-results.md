# Get Results with LOBSTR.IO

Retrieves results from LOBSTR.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/results`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Get Results](https://docs.lobstr.io/docs/get-results)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run` | query | `string` | no | Hash of the run. Use this or Squid, but not both. |
| `squid` | query | `string` | no | Hash of the squid. Use this or Run, but not both. |
| `task` | query | `string` | no | Hash of a specific task to filter results. |
