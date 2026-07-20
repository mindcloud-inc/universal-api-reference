# Execute Workflow with Resco Cloud

Starts a workflow in Resco Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/ExecuteWorkflow`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Execute Workflow](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rawBody` | body | `string` | yes | XML workflow execution body for the Resco ExecuteWorkflow request. |
