# List Concept Relations with Clarifai

Retrieves concept relations from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/{userId}/apps/{{appId}}/concepts/{{conceptId}}/relations`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [List Concept Relations](https://docs.clarifai.com/create/concepts/concepts-relations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Clarifai app ID. |
| `conceptId` | path | `string` | no | Clarifai concept ID. |
