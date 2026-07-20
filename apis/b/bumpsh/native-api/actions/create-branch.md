# Create Branch with Bump.sh

Creates a new branch in Bump.sh.

## Endpoint

- **Method:** `POST`
- **Path:** `docs/:doc_id_or_slug/branches`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Create Branch](https://developers.bump.sh/source.json#/paths/~1docs~1{doc_id_or_slug}~1branches/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doc_id_or_slug` | path | `string` | yes | Documentation ID or slug. |
| `name` | body | `string` | yes | Branch name to create. |
