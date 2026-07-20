# Create Contact with RAYNET CRM

## Endpoint

- **Method:** `PUT`
- **Path:** `person/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Create Contact](https://app.raynetcrm.com/api/doc/index-en.html#tag/Contacts/operation/personInsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastName` | body | `string` | yes | [Last name] |
| `firstName` | body | `string` | no | [Name] |
| `contactInfo.email` | body | `string` | no | [Email] |
| `contactInfo.tel1` | body | `string` | no | [Phone 1] |
| `contactInfo.www` | body | `string` | no | [WWW] |
