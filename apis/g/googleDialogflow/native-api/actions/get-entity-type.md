# Get Entity Type with Google Dialogflow

Retrieves an entity type from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Get Entity Type](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized entity type fields. |
| `name` | path | `string` | no | Required Dialogflow entity type resource name. |
| `name` | path | `string` | yes | Required Dialogflow entity type resource name. |
