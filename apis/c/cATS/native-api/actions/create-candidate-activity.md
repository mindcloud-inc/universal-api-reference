# Create Candidate Activity with CATS

Creates a candidate activity in CATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/candidates/:id/activities`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Create Candidate Activity](https://docs.catsone.com/api/v3/#candidates-create-a-candidate-activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the candidate to create an activity for. |
| `type` | body | `string` | yes | The activity type. |
| `notes` | body | `string` | no | Activity notes. |
