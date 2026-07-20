# List Campaign Leads with LinkedCamp

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [List Campaign Leads](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | query | `string` | yes | Campaign identifier. |
| `status` | query | `string` | no | Optional lead status filter. |
