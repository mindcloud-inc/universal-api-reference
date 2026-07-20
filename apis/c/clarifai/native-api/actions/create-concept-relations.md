# Create Concept Relations with Clarifai

Creates concept relations in Clarifai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/{userId}/apps/{{appId}}/concepts/{{conceptId}}/relations`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Create Concept Relations](https://docs.clarifai.com/create/concepts/concepts-relations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Clarifai app ID. |
| `conceptId` | path | `string` | no | Clarifai concept ID. |
