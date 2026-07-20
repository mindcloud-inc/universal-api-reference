# Get Page with Google Dialogflow

Retrieves a page from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Get Page](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized page fields. |
| `name` | path | `string` | yes | Required Dialogflow page resource name. |
