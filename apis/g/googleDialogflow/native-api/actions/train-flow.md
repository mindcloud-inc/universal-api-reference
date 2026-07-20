# Train Flow with Google Dialogflow

Trains a flow in Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:name:train`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Train Flow](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/train)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required Dialogflow flow resource name. |
| `body` | body | `object` | no | TrainFlowRequest JSON body. |
