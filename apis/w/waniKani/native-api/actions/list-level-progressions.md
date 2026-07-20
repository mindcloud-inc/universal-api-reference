# List Level Progressions with WaniKani

Retrieves level progressions from WaniKani.

## Endpoint

- **Method:** `GET`
- **Path:** `/level_progressions`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [List Level Progressions](https://docs.api.wanikani.com/20170710/#get-all-level-progressions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Filter level progressions by a comma-separated list of IDs. |
| `updated_after` | query | `date` | no | Return level progressions updated after this ISO 8601 timestamp. |
