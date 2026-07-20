# Update Agent with Google Dialogflow

Updates an existing agent in Google Dialogflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Update Agent](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required Dialogflow agent resource name. |
| `body` | body | `object` | yes | Dialogflow Agent fields to update. |
| `updateMask` | query | `string` | no | Optional field mask controlling which agent fields are updated. |
