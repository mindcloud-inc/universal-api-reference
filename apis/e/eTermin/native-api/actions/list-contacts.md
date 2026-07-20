# List Contacts with eTermin

Retrieves contacts from eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/contact`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Contacts](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Contact/get_api_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | E-Mail of the contact |
| `id` | query | `string` | no | ExternalID of the contact |
| `cid` | query | `string` | no | CID of the contact |
| `creationdate` | query | `string` | no | Displays all contacts that were created on this date |
| `creationdateall` | query | `string` | no | Displays all contacts that were created since this date |
