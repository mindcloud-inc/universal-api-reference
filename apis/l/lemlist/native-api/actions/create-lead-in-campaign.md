# Create Lead in Campaign with lemlist

Creates a new lead in a lemlist campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaignId/leads/`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [Create Lead in Campaign](https://developer.lemlist.com/api-reference/endpoints/leads/create-lead-in-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The ID of the campaign to add the lead to. |
| `email` | body | `string` | yes | The lead's email address. |
| `firstName` | body | `string` | no | The lead's first name. |
| `lastName` | body | `string` | no | The lead's last name. |
| `companyName` | body | `string` | no | The lead's company name. |
| `jobTitle` | body | `string` | no | The lead's job title. |
| `linkedinUrl` | body | `string` | no | The lead's LinkedIn profile URL. |
| `picture` | body | `string` | no | The lead's profile picture URL. |
| `phone` | body | `string` | no | The lead's phone number. |
| `companyDomain` | body | `string` | no | The lead's company domain. |
| `icebreaker` | body | `string` | no | A custom icebreaker to personalize outreach. |
| `timezone` | body | `string` | no | The lead's timezone. |
| `contactOwner` | body | `string` | no | The lead owner's email address. |
| `deduplicate` | query | `boolean` | no | Prevents duplicate leads from being added when enabled. |
| `linkedin_enrichment` | query | `boolean` | no | Enrich the lead with LinkedIn data if available. |
| `findEmail` | query | `boolean` | no | Find an email address for the lead when one is not provided. |
| `verifyEmail` | query | `boolean` | no | Verify the provided or found email address. |
| `findPhone` | query | `boolean` | no | Find a phone number for the lead if available. |
