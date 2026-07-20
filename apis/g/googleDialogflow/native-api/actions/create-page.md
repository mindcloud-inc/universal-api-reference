# Create Page with Google Dialogflow

Creates a new page in Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:parent/pages`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Create Page](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized page fields. |
| `parent` | path | `string` | yes | Required parent flow resource name for the new page. |
| `body` | body | `object` | yes | Dialogflow Page request body. |
