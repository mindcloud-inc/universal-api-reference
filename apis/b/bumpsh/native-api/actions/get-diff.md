# Get Diff with Bump.sh

Retrieves a diff from Bump.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `diffs/:id`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Get Diff](https://developers.bump.sh/source.json#/paths/~1diffs~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Diff ID returned by Create Diff. |
