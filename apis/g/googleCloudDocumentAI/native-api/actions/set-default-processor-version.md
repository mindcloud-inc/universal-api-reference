# Set Default Processor Version with Google Cloud Document AI

Sets the default processor version in Google Cloud Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:setDefaultProcessorVersion`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Set Default Processor Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/setDefaultProcessorVersion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | yes | Document AI processor ID. |
| `defaultProcessorVersion` | body | `string` | yes | Full resource name of the processor version to set as default. |
