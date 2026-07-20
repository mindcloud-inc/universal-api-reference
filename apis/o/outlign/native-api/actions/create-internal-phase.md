# Create Internal Phase with Outlign

Creates a new internal phase in Outlign.

## Endpoint

- **Method:** `POST`
- **Path:** `/phases`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [Create Internal Phase](https://go.outlign.co/api/docs/phases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The phase name. |
| `project_id` | body | `number` | yes | The project that owns the phase. |
