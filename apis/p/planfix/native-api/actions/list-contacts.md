# List Contacts with Planfix

Retrieves contacts and companies from Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/list`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [List Contacts](https://help.planfix.com/restapidocs/#/Contact/get-contact-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `string` | no | Comma-delimited contact fields to return. |
| `pageSize` | body | `number` | no | Number of contacts to return. |
| `offset` | body | `number` | no | Contact list offset. |
| `isCompany` | body | `boolean` | no | True for companies, false for people. |
| `filterId` | body | `string` | no | Saved Planfix contact filter identifier. |
