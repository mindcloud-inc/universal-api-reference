# Get Episode Marker with Simplecast

Retrieves an episode marker from Simplecast by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/:episode_id/markers/:marker_id`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [Get Episode Marker](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `episode_id` | path | `string` | yes | Simplecast episode identifier. |
| `marker_id` | path | `string` | yes | Simplecast marker identifier. |
