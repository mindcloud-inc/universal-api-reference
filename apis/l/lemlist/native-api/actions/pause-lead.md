# Pause Lead with lemlist

Pauses an existing lead in lemlist.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/pause/:leadId`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [Pause Lead](https://developer.lemlist.com/api-reference/endpoints/leads/pause-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | The ID of the lead to pause. |
| `campaignId` | query | `string` | no | Pause the lead only in this specific campaign. |
