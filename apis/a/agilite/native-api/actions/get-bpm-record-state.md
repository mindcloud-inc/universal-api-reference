# Get BPM Record State with Agilite

Retrieves a BPM record state from Agilite.

## Endpoint

- **Method:** `GET`
- **Path:** `/bpm/getRecordState`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get BPM Record State](https://docs.agilite.io/reference/getrecordstate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `process-keys` | query | `string` | no | Optional BPM profile key filter; separate multiple keys with commas. |
| `bpm-record-ids` | query | `string` | no | Optional BPM record ID filter; separate multiple IDs with commas. |
