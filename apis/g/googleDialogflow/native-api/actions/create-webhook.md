# Create Webhook with Google Dialogflow

Creates a new webhook in Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:parent/webhooks`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Create Webhook](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.webhooks/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | path | `string` | yes | Required parent agent resource name for the new webhook. |
| `body` | body | `object` | yes | Dialogflow Webhook request body. |
