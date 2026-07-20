# List Posts with StoryChief

Retrieves posts from StoryChief.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [List Posts](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-8d5c14c1-658c-4b29-9b6d-a1dee18f4662)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination_id` | query | `string` | no | Destination ID selector. |
| `destination_type` | query | `string` | no | Post destination type selector. |
| `status` | query | `string` | no | Post status selector. |
