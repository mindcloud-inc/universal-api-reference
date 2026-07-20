# Add Contact Tags by Email with Dynosend

Adds tags to a Dynosend contact by email address.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/addtag`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Add Contact Tags by Email](https://developers.dynosend.com/#tagacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | body | `string` | yes | The UID of the audience that contains the contact. |
| `email` | body | `string` | yes | The email address of the contact to tag. |
| `tag` | body | `string` | yes | A comma-separated tag list to add to the contact. |
