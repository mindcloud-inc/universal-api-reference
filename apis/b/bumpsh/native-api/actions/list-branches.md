# List Branches with Bump.sh

Retrieves branches from a Bump.sh documentation.

## Endpoint

- **Method:** `GET`
- **Path:** `docs/:doc_id_or_slug/branches`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [List Branches](https://developers.bump.sh/source.json#/paths/~1docs~1{doc_id_or_slug}~1branches/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doc_id_or_slug` | path | `string` | yes | Documentation ID or slug. |
