# Get Run Stats with LOBSTR.IO

Retrieves run stats from LOBSTR.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/runs/:run_hash/stats`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Get Run Stats](https://docs.lobstr.io/docs/get-run-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_hash` | path | `string` | yes | The unique identifier (hash) of the run. |
