# Export Agent with Google Dialogflow

Exports an agent from Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:name:export`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Export Agent](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required Dialogflow agent resource name. |
| `body` | body | `object` | no | ExportAgentRequest JSON body. |
