# Create Concepts with Clarifai

Creates concepts in Clarifai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/me/apps/:appId/concepts`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Create Concepts](https://docs.clarifai.com/create/concepts/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `concepts[]` | body | `array<object>` | yes | Concepts to create. |
| `concepts[].id` | body | `string` | yes | Concept ID. |
| `concepts[].name` | body | `string` | yes | Concept name. |
