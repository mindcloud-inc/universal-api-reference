# Update Page with Google Dialogflow

Updates an existing page in Google Dialogflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Update Page](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized page fields. |
| `name` | path | `string` | yes | Required Dialogflow page resource name. |
| `body` | body | `object` | yes | Dialogflow Page fields to update. |
| `updateMask` | query | `string` | no | Optional field mask controlling which page fields are updated. |
