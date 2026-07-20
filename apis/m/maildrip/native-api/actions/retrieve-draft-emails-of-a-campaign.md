# Retrieve draft emails of a campaign with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/campaigns/{campaign_id}/draft-mails`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Retrieve draft emails of a campaign](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of the campaign to retrieve draft emails from |
| `limit` | query | `number` | no | Number of items per page, use "all" for all items |
| `page` | query | `number` | no | Page number for pagination |
