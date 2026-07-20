# Update Flow with Base64.ai

Updates an existing flow in Base64.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/flow/:flowId`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [Update Flow](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `string` | yes | Flow identifier to update. |
| `name` | body | `string` | no | Updated flow name. |
| `status` | body | `string` | no | Updated flow status. |
| `hitl` | body | `object` | no | Updated human-in-the-loop settings object. |
