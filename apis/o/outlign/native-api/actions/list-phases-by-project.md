# List Phases By Project with Outlign

Retrieves project phase records from Outlign by project.

## Endpoint

- **Method:** `GET`
- **Path:** `/phases`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [List Phases By Project](https://go.outlign.co/api/docs/phases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | yes | Filter phases by project ID. |
