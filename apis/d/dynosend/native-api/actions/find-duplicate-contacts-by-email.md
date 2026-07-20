# Find Duplicate Contacts by Email with Dynosend

Finds duplicate contacts in Dynosend by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/duplicate`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Find Duplicate Contacts by Email](https://developers.dynosend.com/#getaduplicatecontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address to check for duplicates across audiences. |
