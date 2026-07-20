# Create Diff with Bump.sh

Creates a diff in Bump.sh.

## Endpoint

- **Method:** `POST`
- **Path:** `diffs`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Create Diff](https://developers.bump.sh/source.json#/paths/~1diffs/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `definition` | body | `string` | yes | Serialized current OpenAPI or AsyncAPI definition. |
| `previous_definition` | body | `string` | yes | Serialized previous OpenAPI or AsyncAPI definition. |
