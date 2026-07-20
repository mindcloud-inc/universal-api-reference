# Delete Annotations with Clarifai

Deletes existing annotations from Clarifai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/users/{userId}/apps/{{appId}}/annotations`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Delete Annotations](https://docs.clarifai.com/create/labeling/api/annotations-delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Clarifai app ID. |
