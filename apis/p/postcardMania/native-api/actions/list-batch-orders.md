# List Batch Orders with PostcardMania

Retrieves orders from a PostcardMania batch.

## Endpoint

- **Method:** `GET`
- **Path:** `/batch/{{batchID}}/orders`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [List Batch Orders](https://docs.pcmintegrations.com/docs/directmail-api/uneg76q9gk3rh)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchID` | path | `string` | no | Internal batch identifier. |
