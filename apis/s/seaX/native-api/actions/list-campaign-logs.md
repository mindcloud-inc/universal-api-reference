# List Campaign Logs with SeaX

Retrieves logs for a SeaX campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{campaign_id}/logs`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [List Campaign Logs](https://api.seasalt.ai/seax/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | Campaign identifier. |
