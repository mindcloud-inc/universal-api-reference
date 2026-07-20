# List Campaigns with Woodpecker.co

Retrieves campaigns from Woodpecker, optionally filtered by status.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1/campaign_list`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [List Campaigns](https://developers.woodpecker.co/docs/campaigns/GET-campaign-list-v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional Woodpecker campaign status filter. |
