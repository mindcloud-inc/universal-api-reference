# Get Prospect Responses with Woodpecker.co

Retrieves responses for a Woodpecker prospect.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/prospects/[:prospect_id]/responses`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Get Prospect Responses](https://developers.woodpecker.co/docs/prospects/GET-prospect-responses/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | query | `number` | no | Filter responses by campaign ID. |
| `prospect_id` | path | `number` | yes | Prospect ID from Woodpecker. |
