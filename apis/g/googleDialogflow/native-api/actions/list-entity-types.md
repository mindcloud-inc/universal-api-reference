# List Entity Types with Google Dialogflow

Retrieves entity types from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:parent/entityTypes`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [List Entity Types](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized entity type fields. |
| `parent` | path | `string` | yes | Required parent agent resource name. |
