# Update Webhook with Google Dialogflow

Updates an existing webhook in Google Dialogflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Update Webhook](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.webhooks/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required Dialogflow webhook resource name. |
| `body` | body | `object` | yes | Dialogflow Webhook fields to update. |
| `updateMask` | query | `string` | no | Optional field mask controlling which webhook fields are updated. |
