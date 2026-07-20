# List Agents with Google Dialogflow

Retrieves agents from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:parent/agents`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [List Agents](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | path | `string` | yes | Required parent location resource name, for example projects/my-project/locations/global. |
