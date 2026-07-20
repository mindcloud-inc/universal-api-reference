# Get Episode Keyword with Simplecast

Retrieves an episode keyword from Simplecast by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/:episode_id/keywords/:keyword_id`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [Get Episode Keyword](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `episode_id` | path | `string` | yes | Simplecast episode identifier. |
| `keyword_id` | path | `string` | yes | Simplecast keyword identifier. |
