# List Snapshots with E2B

Retrieves a list of snapshots from E2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/snapshots`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [List Snapshots](https://e2b.dev/docs/api-reference/sandboxes/get-snapshots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxID` | query | `string` | no | Filter snapshots by source sandbox ID. |
