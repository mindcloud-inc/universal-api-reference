# List Runs with LOBSTR.IO

Retrieves runs from LOBSTR.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/runs`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [List Runs](https://docs.lobstr.io/docs/list-runs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `squid` | query | `string` | yes | The squid hash ID to list runs for. |
