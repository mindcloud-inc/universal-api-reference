# Update Lead in a Campaign with lemlist

Updates an existing lead in a lemlist campaign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaigns/:campaignId/leads/:leadId`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [Update Lead in a Campaign](https://developer.lemlist.com/api-reference/endpoints/leads/update-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The ID of the campaign containing the lead. |
| `leadId` | path | `string` | yes | The ID of the lead to update. |
| `firstName` | body | `string` | no | The lead's first name. |
| `lastName` | body | `string` | no | The lead's last name. |
| `companyName` | body | `string` | no | The lead's company name. |
| `jobTitle` | body | `string` | no | The lead's job title. |
| `preferredContactMethod` | body | `string` | no | Preferred contact method for the lead. |
| `contactOwner` | body | `string` | no | Owner of the contact in lemlist. |
