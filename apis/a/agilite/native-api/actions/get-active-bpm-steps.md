# Get Active BPM Steps with Agilite

Retrieves active BPM steps from Agilite by process key.

## Endpoint

- **Method:** `GET`
- **Path:** `/bpm/getActiveSteps`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Get Active BPM Steps](https://docs.agilite.io/reference/getactivesteps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `process-key` | query | `string` | yes | Agilit-e BPM process key. |
