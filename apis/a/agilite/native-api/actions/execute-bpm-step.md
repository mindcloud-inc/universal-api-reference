# Execute BPM Step with Agilite

Executes a BPM record in Agilite.

## Endpoint

- **Method:** `POST`
- **Path:** `/bpm/execute`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Execute BPM Step](https://docs.agilite.io/reference/execute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `process-key` | query | `string` | yes | Agilit-e BPM process key. |
| `bpm-record-id` | query | `string` | yes | BPM record identifier. |
| `option-selected` | query | `string` | yes | Selected BPM step option. |
| `current-user` | query | `string` | yes | User executing the BPM step. |
| `comments` | query | `string` | no | Optional execution comments. |
| `current-step` | query | `string` | yes | Current step key or name for the BPM record. |
| `data` | body | `object` | no | Optional JSON body sent to the BPM execution endpoint. |
