# Get Spaced Repetition System with WaniKani

Retrieves a spaced repetition system from WaniKani.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaced_repetition_systems/:id`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [Get Spaced Repetition System](https://docs.api.wanikani.com/20170710/#get-a-specific-spaced-repetition-system)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The spaced repetition system ID to retrieve. |
