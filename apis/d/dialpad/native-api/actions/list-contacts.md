# List Contacts with Dialpad

Retrieves shared or local contacts from Dialpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Contacts](https://developers.dialpad.com/reference/contactslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |
| `include_local` | query | `boolean` | no | If set to true company local contacts will be included. |
| `owner_id` | query | `string` | no | The id of the user who owns the contact. |
