# List Episode Authors with Simplecast

Retrieves authors for an episode from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/:episode_id/authors`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Episode Authors](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `episode_id` | path | `string` | yes | Simplecast episode identifier. |
