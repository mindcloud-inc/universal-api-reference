# List Episode Keywords with Simplecast

Retrieves keywords for an episode from Simplecast.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/:episode_id/keywords`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [List Episode Keywords](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `episode_id` | path | `string` | yes | Simplecast episode identifier. |
