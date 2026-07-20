# Delete Entity Type with Google Dialogflow

Deletes an existing entity type from Google Dialogflow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v3/:name`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [Delete Entity Type](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required Dialogflow entity type resource name. |
| `force` | query | `boolean` | no | Optional flag to force deletion when the provider supports it. |
