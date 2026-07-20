# Create Entity Type with Google Dialogflow

Creates a new entity type in Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:parent/entityTypes`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Create Entity Type](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized entity type fields. |
| `parent` | path | `string` | yes | Required parent agent resource name for the new entity type. |
| `body` | body | `object` | yes | Dialogflow EntityType request body. |
