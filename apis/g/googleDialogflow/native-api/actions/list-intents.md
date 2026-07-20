# List Intents with Google Dialogflow

Retrieves intents from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:parent/intents`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [List Intents](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.intents/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intentView` | query | `string` | no | Optional intent view controlling how much intent data is returned. |
| `parent` | path | `string` | yes | Required parent agent resource name. |
