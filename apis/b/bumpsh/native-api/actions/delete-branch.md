# Delete Branch with Bump.sh

Deletes an existing branch from Bump.sh.

## Endpoint

- **Method:** `DELETE`
- **Path:** `docs/:doc_id_or_slug/branches/:slug`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Delete Branch](https://developers.bump.sh/source.json#/paths/~1docs~1{doc_id_or_slug}~1branches~1{slug}/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doc_id_or_slug` | path | `string` | yes | Documentation ID or slug. |
| `slug` | path | `string` | yes | Branch slug to delete. |
