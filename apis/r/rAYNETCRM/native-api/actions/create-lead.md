# Create Lead with RAYNET CRM

## Endpoint

- **Method:** `PUT`
- **Path:** `lead/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Create Lead](https://app.raynetcrm.com/api/doc/index-en.html#tag/Leads/operation/leadInsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyName` | body | `string` | no | Lead company name. |
| `contactInfo.email` | body | `string` | no | Lead email address. |
| `contactInfo.tel1` | body | `string` | no | Lead primary phone number. |
| `contactInfo.www` | body | `string` | no | Lead website URL. |
| `firstName` | body | `string` | no | Lead first name. |
| `lastName` | body | `string` | no | Lead last name. |
| `priority` | body | `string` | yes | Lead priority. |
| `topic` | body | `string` | yes | Lead topic. |
