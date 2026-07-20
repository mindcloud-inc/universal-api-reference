# Poll Async Generation Request with Abyssale

Retrieves an async generation request status from Abyssale.

## Endpoint

- **Method:** `GET`
- **Path:** `/generation-request/:generation_request_id`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Poll Async Generation Request](https://developers.abyssale.com/rest-api/generation/asynchronous-generation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `generation_request_id` | path | `string` | yes |
