# Get App Workflow with Clappia

Retrieves app workflow details from Clappia.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflowdefinitionv2/getWorkflow`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Get App Workflow](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | yes | Clappia app ID. |
| `triggerType` | query | `string` | yes | Workflow trigger type such as newSubmission, editSubmission, or reviewSubmission. |
