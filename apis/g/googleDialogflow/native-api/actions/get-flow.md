# Get Flow with Google Dialogflow

Retrieves a flow from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Get Flow](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized flow fields. |
| `name` | path | `string` | yes | Required Dialogflow flow resource name. |
