# Delete Contact by Identifier with SuperSend

Deletes contacts from SuperSend by identifier.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Delete Contact by Identifier](https://docs.supersend.io/docs/contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TeamId` | query | `string` | yes | — |
| `CampaignId` | query | `string` | yes | — |
| `email` | query | `string` | no | Email address to delete (required if no linkedin_url) |
| `linkedin_url` | query | `string` | no | LinkedIn URL to delete (required if no email) |
