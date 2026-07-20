# Delete Webhook with Google Dialogflow

Deletes an existing webhook from Google Dialogflow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Delete Webhook](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.webhooks/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required Dialogflow webhook resource name. |
| `force` | query | `boolean` | no | Optional flag to force deletion when the provider supports it. |
