# Create URL Source with Chatsistant

Creates a new URL source in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/data-source/url`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Create URL Source](https://docs.chatsistant.com/api-reference/data-sources/create-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | The source URL. |
| `uuid` | path | `string` | no | The chatbot UUID. |
