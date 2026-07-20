# Export Flow with Google Dialogflow

Exports a flow from Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:name:export`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Export Flow](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required Dialogflow flow resource name. |
| `body` | body | `object` | no | ExportFlowRequest JSON body. |
