# List Playbooks with Devin

Retrieves a list of playbooks from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/playbooks`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [List Playbooks](https://docs.devin.ai/api-reference/v3/playbooks/organizations-playbooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
