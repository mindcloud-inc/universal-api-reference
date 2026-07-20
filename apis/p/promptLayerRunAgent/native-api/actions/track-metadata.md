# Track Metadata with PromptLayer Run Agent

Tracks metadata in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/track-metadata`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Track Metadata](https://docs.promptlayer.com/reference/track-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | body | `number` | yes | The unique identifier for the request to which the metadata is associated. |
| `metadata` | body | `object` | yes | A dictionary of metadata items to associate with the request. |
