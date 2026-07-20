# Set Default Branch with Bump.sh

Sets the default branch for a Bump.sh documentation.

## Endpoint

- **Method:** `PATCH`
- **Path:** `docs/:doc_id_or_slug/branches/:slug/set_default`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Set Default Branch](https://developers.bump.sh/source.json#/paths/~1docs~1{doc_id_or_slug}~1branches~1{slug}~1set_default/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doc_id_or_slug` | path | `string` | yes | Documentation ID or slug. |
| `slug` | path | `string` | yes | Branch slug to promote. |
