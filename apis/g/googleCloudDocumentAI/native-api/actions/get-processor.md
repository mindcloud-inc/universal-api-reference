# Get Processor with Google Cloud Document AI

Retrieves a processor from Google Cloud Document AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Get Processor](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | yes | Processor ID from projects/{project}/locations/{location}/processors/{processor}. |
