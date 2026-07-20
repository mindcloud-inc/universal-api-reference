# Create Source Tag with Chatsistant

Creates a new source tag in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/source-tag/create`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Create Source Tag](https://docs.chatsistant.com/api-reference/source-tags/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | The source tag color. |
| `name` | body | `string` | no | The source tag name. |
| `uuid` | path | `string` | no | The chatbot UUID. |
