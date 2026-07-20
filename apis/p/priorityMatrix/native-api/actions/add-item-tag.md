# Add Item Tag with Priority Matrix

Adds a tag to a Priority Matrix item.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tag/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Add Item Tag](https://sync.appfluence.com/developer/guide/#concrete-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object` | body | `string` | yes | Item resource URI to tag. |
| `name` | body | `string` | yes | Tag name. |
