# Get Active BPM Users with Agilite

Retrieves active BPM users from Agilite by process key.

## Endpoint

- **Method:** `GET`
- **Path:** `/bpm/getActiveUsers`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Active BPM Users](https://docs.agilite.io/reference/getactiveusers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `process-key` | query | `string` | yes | Agilit-e BPM process key. |
