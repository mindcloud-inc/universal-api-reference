# List Pages with Google Dialogflow

Retrieves pages from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:parent/pages`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [List Pages](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized page fields. |
| `parent` | path | `string` | yes | Required parent flow resource name. |
