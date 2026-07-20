# Create or Update Lead with LaGrowthMachine

Creates or updates a lead in LaGrowthMachine.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [Create or Update Lead](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience` | body | `string` | yes | Audience name. |
| `bio` | body | `string` | no | Lead bio. |
| `companyName` | body | `string` | no | Lead company name. |
| `companyUrl` | body | `string` | no | Lead company URL. |
| `crm_id` | body | `string` | no | Lead CRM ID. |
| `customAttribute1` | body | `string` | no | Lead custom attribute 1. |
| `customAttribute10` | body | `string` | no | Lead custom attribute 10. |
| `customAttribute2` | body | `string` | no | Lead custom attribute 2. |
| `customAttribute3` | body | `string` | no | Lead custom attribute 3. |
| `customAttribute4` | body | `string` | no | Lead custom attribute 4. |
| `customAttribute5` | body | `string` | no | Lead custom attribute 5. |
| `customAttribute6` | body | `string` | no | Lead custom attribute 6. |
| `customAttribute7` | body | `string` | no | Lead custom attribute 7. |
| `customAttribute8` | body | `string` | no | Lead custom attribute 8. |
| `customAttribute9` | body | `string` | no | Lead custom attribute 9. |
| `excludeContactedLeads` | body | `boolean` | no | Exclude leads who have already been contacted. |
| `firstname` | body | `string` | no | Lead first name. |
| `gender` | body | `string` | no | Lead gender. Accepted values are `man` or `woman`. |
| `industry` | body | `string` | no | Lead industry. |
| `jobTitle` | body | `string` | no | Lead job title. |
| `lastname` | body | `string` | no | Lead last name. |
| `leadId` | body | `string` | no | Existing lead ID to update. |
| `linkedinUrl` | body | `string` | no | Lead LinkedIn URL. |
| `location` | body | `string` | no | Lead location. |
| `persoEmail` | body | `string` | no | Lead personal email. |
| `phone` | body | `string` | no | Lead phone number. |
| `proEmail` | body | `string` | no | Lead professional email. |
| `profilePicture` | body | `string` | no | Lead profile picture URL. |
| `twitter` | body | `string` | no | Lead Twitter profile URL or handle. |
