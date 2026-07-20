# Add Item Comment with Priority Matrix

Creates a new comment on a Priority Matrix item.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/comment/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Add Item Comment](https://sync.appfluence.com/developer/guide/#concrete-examples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item` | body | `string` | yes | Item resource URI, for example /api/v1/item/345/. |
| `text` | body | `string` | yes | Comment text. |
