# Delete user from campaign with Maildrip

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/campaigns/{campaign_id}/{recipient_id}/user`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Delete user from campaign](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of the campaign |
| `recipient_id` | path | `string` | yes | ID of the recipient to delete |
