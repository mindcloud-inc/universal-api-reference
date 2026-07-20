# Update Contact with RAYNET CRM

## Endpoint

- **Method:** `POST`
- **Path:** `person/:personId/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Update Contact](https://app.raynetcrm.com/api/doc/index-en.html#tag/Contacts/operation/personEdit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | path | `string` | yes | contact ID |
| `firstName` | body | `string` | no | [Name] |
| `lastName` | body | `string` | no | [Last name] |
| `contactInfo.email` | body | `string` | no | [Email] |
| `contactInfo.tel1` | body | `string` | no | [Phone 1] |
| `contactInfo.www` | body | `string` | no | [WWW] |
