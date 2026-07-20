# List Spaced Repetition Systems with WaniKani

Retrieves spaced repetition systems from WaniKani.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaced_repetition_systems`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [List Spaced Repetition Systems](https://docs.api.wanikani.com/20170710/#get-all-spaced-repetition-systems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Filter spaced repetition systems by a comma-separated list of IDs. |
| `updated_after` | query | `date` | no | Return spaced repetition systems updated after this ISO 8601 timestamp. |
