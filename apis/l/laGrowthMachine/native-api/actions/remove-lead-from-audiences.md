# Remove Lead from Audiences with LaGrowthMachine

Removes a lead from audiences in LaGrowthMachine.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/removefromaudience`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [Remove Lead from Audiences](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience[]` | body | `array<string>` | yes | Audience names to remove from the lead, or use `all` to remove the lead from every audience. |
| `companyName` | body | `string` | no | Lead company name. |
| `companyUrl` | body | `string` | no | Lead company URL. |
| `crm_id` | body | `string` | no | Lead CRM ID. |
| `firstname` | body | `string` | no | Lead first name. |
| `lastname` | body | `string` | no | Lead last name. |
| `linkedinUrl` | body | `string` | no | Lead LinkedIn URL. |
| `persoEmail` | body | `string` | no | Lead personal email. |
| `proEmail` | body | `string` | no | Lead professional email. |
| `twitter` | body | `string` | no | Lead Twitter profile URL or handle. |
