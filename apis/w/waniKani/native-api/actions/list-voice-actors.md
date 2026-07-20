# List Voice Actors with WaniKani

Retrieves voice actors from WaniKani.

## Endpoint

- **Method:** `GET`
- **Path:** `/voice_actors`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [List Voice Actors](https://docs.api.wanikani.com/20170710/#get-all-voice-actors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Filter voice actors by a comma-separated list of IDs. |
| `updated_after` | query | `date` | no | Return voice actors updated after this ISO 8601 timestamp. |
