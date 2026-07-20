# Create Chatflow with FlowiseAI

Creates a new chatflow in FlowiseAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatflows`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Create Chatflow](https://docs.flowiseai.com/api-reference/chatflows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON body with documented chatflow fields such as name, flowData, deployed, and isPublic. |
