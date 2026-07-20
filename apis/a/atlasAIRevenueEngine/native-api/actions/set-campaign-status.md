# Set Campaign Status with Atlas AI Revenue Engine

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaign/:campaignId/status`
- **Base URL:** `https://api.youratlas.com/v1/api`
- **Official documentation:** [Set Campaign Status](https://apidocs.youratlas.com/set-campaign-status-26124567e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The campaign ID. |
| `enabled` | body | `boolean` | yes | Enable or disable the campaign. |
