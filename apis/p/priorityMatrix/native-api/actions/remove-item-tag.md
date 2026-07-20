# Remove Item Tag with Priority Matrix

Removes a tag from a Priority Matrix item.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tag/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Remove Item Tag](https://sync.appfluence.com/developer/guide/#concrete-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object` | body | `string` | yes | Item resource URI to untag. |
| `name` | body | `string` | yes | Tag name. |
