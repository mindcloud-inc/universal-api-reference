# Delete Voice with Runway

Deletes a voice from Runway.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/voices/[:id]`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Delete Voice](https://docs.dev.runwayml.com/api#tag/Voices/paths/~1v1~1voices~1%7Bid%7D/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the voice to delete. |
