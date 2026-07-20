# Import Campaign List with Sarbacane

Imports a list into a campaign in Sarbacane.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/{campaignId}/list`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Import Campaign List](https://developers.sarbacane.com/campaigns/#import-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | no | Sarbacane campaign ID. |
| `listId` | body | `string` | no | Sarbacane list ID to import into the campaign. |
