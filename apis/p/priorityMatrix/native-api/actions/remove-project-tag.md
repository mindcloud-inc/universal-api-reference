# Remove Project Tag with Priority Matrix

Removes a tag from a Priority Matrix project.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tag/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Remove Project Tag](https://sync.appfluence.com/developer/guide/#concrete-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object` | body | `string` | yes | Project resource URI to untag. |
| `name` | body | `string` | yes | Tag name. |
