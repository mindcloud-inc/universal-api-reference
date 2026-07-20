# List Flows with Google Dialogflow

Retrieves flows from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:parent/flows`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [List Flows](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized flow fields. |
| `parent` | path | `string` | yes | Required parent agent resource name. |
