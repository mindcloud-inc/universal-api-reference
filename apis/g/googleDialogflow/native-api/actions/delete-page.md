# Delete Page with Google Dialogflow

Deletes an existing page from Google Dialogflow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Delete Page](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required Dialogflow page resource name. |
| `force` | query | `boolean` | no | Optional flag to force deletion when the provider supports it. |
