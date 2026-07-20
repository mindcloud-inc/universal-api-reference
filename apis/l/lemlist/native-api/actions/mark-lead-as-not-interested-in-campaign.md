# Mark Lead as Not Interested in Campaign with lemlist

Marks a lead as not interested in a lemlist campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaignId/leads/:leadIdOrEmail/notinterested`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [Mark Lead as Not Interested in Campaign](https://developer.lemlist.com/api-reference/endpoints/leads/mark-lead-as-not-interested-in-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The ID of the campaign containing the lead. |
| `leadIdOrEmail` | path | `string` | yes | The lead identifier or email address. |
