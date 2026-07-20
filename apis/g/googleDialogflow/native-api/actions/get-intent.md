# Get Intent with Google Dialogflow

Retrieves an intent from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Get Intent](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.intents/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized intent fields. |
| `name` | path | `string` | yes | Required Dialogflow intent resource name. |
