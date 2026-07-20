# List Webhooks with Google Dialogflow

Retrieves webhooks from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:parent/webhooks`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [List Webhooks](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.webhooks/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | path | `string` | yes | Required parent agent resource name. |
