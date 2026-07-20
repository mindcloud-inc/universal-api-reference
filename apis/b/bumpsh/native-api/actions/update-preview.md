# Update Preview with Bump.sh

Updates an existing preview in Bump.sh.

## Endpoint

- **Method:** `PUT`
- **Path:** `previews/:preview_id`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Update Preview](https://developers.bump.sh/source.json#/paths/~1previews~1{preview_id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `definition` | body | `string` | yes | Serialized OpenAPI or AsyncAPI definition used to update the preview. |
| `preview_id` | path | `string` | yes | Preview ID returned by Create Preview. |
