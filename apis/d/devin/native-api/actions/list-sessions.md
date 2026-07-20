# List Sessions with Devin

Retrieves a list of sessions from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/sessions`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [List Sessions](https://docs.devin.ai/api-reference/v3/sessions/enterprise-sessions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
