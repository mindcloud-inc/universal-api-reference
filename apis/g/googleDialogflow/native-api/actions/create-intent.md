# Create Intent with Google Dialogflow

Creates a new intent in Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:parent/intents`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Create Intent](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.intents/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized intent fields. |
| `parent` | path | `string` | yes | Required parent agent resource name for the new intent. |
| `body` | body | `object` | yes | Dialogflow Intent request body. |
