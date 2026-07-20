# List Auto Dialer Campaign Logs with SeaX

Retrieves logs for a SeaX auto dialer campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/auto_dialer_campaigns/{auto_dialer_campaign_id}/logs`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [List Auto Dialer Campaign Logs](https://api.seasalt.ai/seax/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_dialer_campaign_id` | path | `string` | yes | Auto dialer campaign identifier. |
