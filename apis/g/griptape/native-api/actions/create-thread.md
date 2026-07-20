# Create Thread with Griptape

Creates a new thread in Griptape.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/threads`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Create Thread](https://docs.griptape.ai/stable/griptape-cloud/threads/threads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias` | body | `string` | no | Optional unique alias for the thread. |
| `name` | body | `string` | no | Optional thread name to create. |
