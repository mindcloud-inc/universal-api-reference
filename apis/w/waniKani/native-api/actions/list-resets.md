# List Resets with WaniKani

Retrieves resets from WaniKani.

## Endpoint

- **Method:** `GET`
- **Path:** `/resets`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [List Resets](https://docs.api.wanikani.com/20170710/#get-all-resets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Filter resets by a comma-separated list of IDs. |
| `updated_after` | query | `date` | no | Return resets updated after this ISO 8601 timestamp. |
