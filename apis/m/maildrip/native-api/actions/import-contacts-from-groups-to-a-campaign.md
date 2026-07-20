# Import contacts from groups to a campaign with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaigns/{campaign_id}/contacts`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Import contacts from groups to a campaign](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of the campaign to import contacts to |
