# Track Score with PromptLayer Run Agent

Tracks scores in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/track-score`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Track Score](https://docs.promptlayer.com/reference/track-score)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | body | `number` | yes | The request_id from tracking a request. |
| `score` | body | `number` | yes | The score you would like to give to this request (0 - 100). |
| `name` | body | `string` | no | A name for this request score. If omitted, the score is tracked as default. |
