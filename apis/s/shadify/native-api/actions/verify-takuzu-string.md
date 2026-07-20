# Verify Takuzu String with Shadify

Retrieves a Takuzu validation result from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/takuzu/verifier`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Verify Takuzu String](https://shadify.yurace.pro/modules/takuzu.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task` | query | `string` | yes | Required Takuzu rows joined by dashes, containing only 0 and 1. |
