# Download Campaign Logs with SeaX

Retrieves a log download for a SeaX campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{campaign_id}/download_logs`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [Download Campaign Logs](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | Campaign identifier. |
