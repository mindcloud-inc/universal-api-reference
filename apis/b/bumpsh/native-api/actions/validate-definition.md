# Validate Definition with Bump.sh

Validates a documentation definition in Bump.sh.

## Endpoint

- **Method:** `POST`
- **Path:** `validations`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Validate Definition](https://developers.bump.sh/source.json#/paths/~1validations/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `definition` | body | `string` | yes | Serialized OpenAPI or AsyncAPI definition to validate. |
