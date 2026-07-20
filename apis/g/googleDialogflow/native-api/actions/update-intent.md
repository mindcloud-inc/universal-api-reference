# Update Intent with Google Dialogflow

Updates an existing intent in Google Dialogflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Update Intent](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.intents/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized intent fields. |
| `name` | path | `string` | yes | Required Dialogflow intent resource name. |
| `body` | body | `object` | yes | Dialogflow Intent fields to update. |
| `updateMask` | query | `string` | no | Optional field mask controlling which intent fields are updated. |
