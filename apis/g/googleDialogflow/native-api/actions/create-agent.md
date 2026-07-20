# Create Agent with Google Dialogflow

Creates a new agent in Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:parent/agents`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Create Agent](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | path | `string` | yes | Required parent location resource name for the new agent. |
| `body` | body | `object` | yes | Dialogflow Agent request body. |
