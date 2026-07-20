# Create Flow with Google Dialogflow

Creates a new flow in Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:parent/flows`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Create Flow](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized flow fields. |
| `parent` | path | `string` | yes | Required parent agent resource name for the new flow. |
| `body` | body | `object` | yes | Dialogflow Flow request body. |
