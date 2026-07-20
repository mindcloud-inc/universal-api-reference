# Create Campaign Draft with GMass

Creates a Gmail draft for a GMass campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigndrafts`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [Create Campaign Draft](https://api.gmass.co/docs#tag/CampaignDrafts/operation/CampaignDrafts_Index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subject` | body | `string` | yes |
| `message` | body | `string` | yes |
| `fromEmail` | body | `string` | no |
| `messageType` | body | `string` | no |
| `listAddress` | body | `string` | no |
| `emailAddresses` | body | `string` | no |
| `cc` | body | `string` | no |
| `bcc` | body | `string` | no |
| `attachments[]` | body | `array<object>` | no |
| `attachments[].fileName` | body | `string` | no |
| `attachments[].base64Content` | body | `string` | no |
| `attachments[].contentType` | body | `string` | no |
