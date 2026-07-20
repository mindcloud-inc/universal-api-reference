# Get Voice with Runway

Retrieves a voice from Runway.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/voices/[:id]`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Get Voice](https://docs.dev.runwayml.com/api#tag/Voices/paths/~1v1~1voices~1%7Bid%7D/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the voice to retrieve. |
