# Join a campaign as a guest with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaigns/{campaign_id}/join-as-guest`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Join a campaign as a guest](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | ID of the campaign to join |
| `name` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `metadata` | body | `object` | no | — |
