# List Stories with StoryChief

Retrieves stories from StoryChief.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [List Stories](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-f369ebc9-08eb-4b19-880a-1028b9052e73)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lang` | query | `string` | no | Language selector documented as lang. |
| `source` | query | `number` | no | Source ID selector documented as source. |
| `status` | query | `string` | no | Story status selector documented as status. |
| `updated_after` | query | `date` | no | Only return stories updated after this timestamp. |
| `author_id` | query | `number` | no | Author ID selector documented as author_id. |
