# Get Flow Validation Result with Google Dialogflow

Retrieves a flow validation result from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Get Flow Validation Result](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/getValidationResult)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageCode` | query | `string` | no | Optional BCP-47 language code for localized validation result fields. |
| `name` | path | `string` | yes | Required flow validation result resource name. |
