# Update Contact with Documo

Updates an existing contact in Documo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/contacts/:contactId`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Update Contact](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | String \| Required \| Contact UUID |
| `name` | body | `string` | no | String \| Contact name |
| `email` | body | `string` | no | String \| Contact email |
| `faxNumber` | body | `string` | no | String \| Fax number in E164 or number format with country code included |
| `phoneNumber` | body | `string` | no | String \| Phone number in E164 or number format with country code included |
| `organizationId` | body | `string` | no | String \| Assign contact to existing organization contact |
| `isPublic` | body | `boolean` | no | Boolean \| Show contact for all users in the account |
| `isOrganization` | body | `boolean` | no | Boolean \| Create an organization contact when true |
| `publicEditable` | body | `boolean` | no | Boolean \| Allow all account users to edit the contact when true |
