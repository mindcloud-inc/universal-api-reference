# Create Flow with Base64.ai

Creates a new flow in Base64.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/flow`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [Create Flow](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the Base64.ai flow. |
| `status` | body | `string` | no | Flow status, usually enabled. |
| `hitl` | body | `object` | no | Human-in-the-loop settings object. |
