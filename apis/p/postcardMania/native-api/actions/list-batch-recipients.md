# List Batch Recipients with PostcardMania

Retrieves recipients from a PostcardMania batch.

## Endpoint

- **Method:** `GET`
- **Path:** `/batch/{{batchID}}/recipients`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [List Batch Recipients](https://docs.pcmintegrations.com/docs/directmail-api/2cd98e3e8dc89)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchID` | path | `string` | no | Internal batch identifier. |
