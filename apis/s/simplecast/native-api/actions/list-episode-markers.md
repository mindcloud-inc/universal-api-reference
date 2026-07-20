# List Episode Markers with Simplecast

Retrieves markers for an episode from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/:episode_id/markers`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Episode Markers](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `episode_id` | path | `string` | yes | Simplecast episode identifier. |
