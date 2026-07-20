# Update campaign status with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/campaigns/{campaign_id}/status`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Update campaign status](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of the campaign to update status |
| `status` | body | `boolean` | no | New status of the campaign |
