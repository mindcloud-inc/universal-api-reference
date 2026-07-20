# Import Flow with Google Dialogflow

Imports a flow into Google Dialogflow.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/:parent/flows:import`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Import Flow](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | path | `string` | yes | Required parent agent resource name for flow import. |
| `body` | body | `object` | yes | ImportFlowRequest JSON body. |
