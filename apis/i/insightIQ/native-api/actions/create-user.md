# Create User with InsightIQ

Creates a new user in InsightIQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create User](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | yes | Your stable external identifier for the user. |
| `name` | body | `string` | yes | Display name for the InsightIQ user. |
