# Get User By External ID with InsightIQ

Finds a user in InsightIQ by external ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/external_id/:external_id`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get User By External ID](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | path | `string` | yes | External identifier for the InsightIQ user. |
