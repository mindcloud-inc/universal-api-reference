# Delete a campaign variable with Maildrip

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/campaigns/{campaign_id}/variables`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Delete a campaign variable](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of the campaign to delete variables from |
| `name` | query | `string` | yes | Name of the variable to delete |
