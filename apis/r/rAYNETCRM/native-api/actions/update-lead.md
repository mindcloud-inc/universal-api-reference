# Update Lead with RAYNET CRM

## Endpoint

- **Method:** `POST`
- **Path:** `lead/:leadId/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Update Lead](https://app.raynetcrm.com/api/doc/index-en.html#tag/Leads/operation/leadEdit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyName` | body | `string` | no | Lead company name. |
| `contactInfo.email` | body | `string` | no | Lead email address. |
| `contactInfo.tel1` | body | `string` | no | Lead primary phone number. |
| `contactInfo.www` | body | `string` | no | Lead website URL. |
| `firstName` | body | `string` | no | Lead first name. |
| `lastName` | body | `string` | no | Lead last name. |
| `leadId` | path | `string` | yes | Raynet lead identifier. |
| `priority` | body | `string` | no | Lead priority. |
| `topic` | body | `string` | no | Lead topic. |
