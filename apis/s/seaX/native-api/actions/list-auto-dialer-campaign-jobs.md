# List Auto Dialer Campaign Jobs with SeaX

Retrieves jobs for a SeaX auto dialer campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/auto_dialer_campaigns/{auto_dialer_campaign_id}/jobs`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [List Auto Dialer Campaign Jobs](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_dialer_campaign_id` | path | `string` | yes | Auto dialer campaign identifier. |
