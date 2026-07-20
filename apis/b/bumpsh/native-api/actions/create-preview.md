# Create Preview with Bump.sh

Creates a preview in Bump.sh.

## Endpoint

- **Method:** `POST`
- **Path:** `previews`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Create Preview](https://developers.bump.sh/source.json#/paths/~1previews/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `definition` | body | `string` | yes | Serialized OpenAPI or AsyncAPI definition to preview. |
