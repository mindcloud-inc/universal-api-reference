# Update Flow with Google Dialogflow

Updates an existing flow in Google Dialogflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Update Flow](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized flow fields. |
| `name` | path | `string` | yes | Required Dialogflow flow resource name. |
| `body` | body | `object` | yes | Dialogflow Flow fields to update. |
| `updateMask` | query | `string` | no | Optional field mask controlling which flow fields are updated. |
