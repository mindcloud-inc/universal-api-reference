# Update Entity Type with Google Dialogflow

Updates an existing entity type in Google Dialogflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Update Entity Type](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized entity type fields. |
| `name` | path | `string` | yes | Required Dialogflow entity type resource name. |
| `body` | body | `object` | yes | Dialogflow EntityType fields to update. |
| `updateMask` | query | `string` | no | Optional field mask controlling which entity type fields are updated. |
