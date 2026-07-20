# Create Tag with Wooxy

Creates a new tag in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/tags/create`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Create Tag](https://wooxy.com/api-documentation/tags/create-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tag name. |
| `description` | body | `string` | no | Optional tag description. |
