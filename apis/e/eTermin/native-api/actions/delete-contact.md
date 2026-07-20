# Delete Contact with eTermin

Deletes an existing contact from eTermin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/contact`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Delete Contact](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Contact/delete_api_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | E-Mail of the contact (this can lead to the deletion of multiple contacts with the same Email) |
| `id` | query | `string` | no | ExternalID of the contact |
| `cid` | query | `string` | no | CID of the contact |
