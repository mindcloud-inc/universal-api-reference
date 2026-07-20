# Register BPM Record with Agilite

Registers a new BPM record in Agilite.

## Endpoint

- **Method:** `GET`
- **Path:** `/bpm/registerBPMRecord`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Register BPM Record](https://docs.agilite.io/reference/registerbpmrecord)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `process-key` | query | `string` | yes | Agilit-e BPM process key. |
| `current-user` | query | `string` | yes | User initiating the BPM registration. |
